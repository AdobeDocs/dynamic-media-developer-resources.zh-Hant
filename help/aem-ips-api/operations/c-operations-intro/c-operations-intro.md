---
description: 描述由IPS Web Service API處理的常見操作參數。
solution: Experience Manager
title: 操作方法
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---

# 操作方法{#operations-methods}

本節介紹由IPS Web Service API處理的常見操作參數。

有關每個操作參數的完整說明，請參閱[操作參數](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md)。

## 句柄：關於 {#section-094ce1afa6244fa5b2c762f44ffdca1c}

處理某些API操作返回的引用IPS對象。 您也可以將控點作為參數傳遞至後續的操作呼叫。 句柄是字串資料類型(`xsd:string`)。

句柄僅用於單個應用程式會話期間。 此外，應使句柄保持持久性，因為它們的格式可以在IPS版本之間更改。 在編寫互動式應用程式時，您會實施會話超時並放棄會話之間的所有句柄，特別是在IPS升級之後。 在編寫非互動式應用程式時，請調用適當的操作以在每次運行應用程式時檢索句柄。 下列Java/Axis2程式碼範例顯示程式碼執行不正確且正確：

**句柄代碼不正確**

此程式碼範例不正確，因為其包含公司控制代碼的硬式編碼值(555)。

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**正確處理代碼**

此代碼示例正確，因為它調用`getCompanyInfo`以返回有效句柄。 它不依賴硬式編碼值。 使用此方法（或其他等效的IPS API）返回所需的句柄。

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## 常見控制代碼類型 {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

大多數操作都要求您傳遞`companyHandle`參數來設定公司內容。 公司句柄是某些操作（如`getCompanyInfo`、`addCompany`和`getCompanyMembership`）返回的指針。

**userHandle**

`userHandle`參數是針對特定使用者之作業的選用參數。 預設情況下，這些操作將目標定位為調用用戶（其憑據被傳入以進行身份驗證的用戶）。 不過，具有適當權限的管理員使用者可以指定不同的使用者。 例如， `setPassword`操作通常會設定已驗證用戶的密碼，但管理員可以使用`userHandle`參數為不同用戶設定密碼。

對於需要公司上下文（使用`companyHandle`參數）的操作，已驗證和目標用戶都必須是指定公司的成員。 對於不需要公司內容的操作，已驗證和目標使用者必須同時是至少一個共同公司的成員。

以下操作可以檢索用戶句柄：

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle和accessGroupHandle**

依預設，需要存取權限（讀、寫、刪除）的操作會在呼叫使用者的權限內容中執行。 某些操作允許您使用`accessUserHandle`或`accessGroupHandle`參數修改此上下文。 `accessUserHandle`參數可讓管理員模擬其他使用者。 `accessGroupHandle`參數允許調用者在特定用戶組的上下文中操作。

**responseFieldArray和excludeFieldArray**

某些操作允許調用方限制響應中包含哪些欄位。 限制欄位有助於減少處理請求所需的時間和記憶體，並減少回應資料的大小。 調用方可以通過傳遞`responseFieldArray`參數或通過`excludeFieldArray`參數枚舉排除欄位清單來請求特定欄位清單。

`responseFieldArray`和`excludeFieldArray`都使用由`/`分隔的節點路徑指定欄位。 例如，若要指定`searchAssets`僅傳回每個資產的名稱、上次修改日期和中繼資料，請參閱下列內容：

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

同樣地，若要傳回所有欄位（權限除外）:

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

請注意，節點路徑是相對於返回節點根的。 如果指定一個不含任何子元素的複雜類型欄位（例如`assetArray/items/imageInfo`），則其所有子元素都將包括在內。 如果在複雜類型欄位中指定一個或多個子元素（例如`assetArray/items/imageInfo/originalPath`），則只包括那些子元素。

若您未在請求中納入`responseFieldArray`或`excludeFieldArray`，則會傳回所有欄位。

**地區設定**

自IPS 4.0起，IPS API支援通過傳遞`authHeader`區域設定參數來設定操作的區域設定上下文。 如果區域設定參數不存在，則將使用HTTP標題`Accept-Language`。 如果此標頭不存在，則使用IPS伺服器的預設區域設定。

某些操作還採用顯式語言環境參數，這些參數可能與操作語言環境上下文不同。 例如， `submitJob`操作採用`locale`參數，該參數設定用於作業記錄和電子郵件通知的區域設定。

地區設定參數使用`<language_code>[-<country_code>]`格式

其中，語言代碼是ISO-639指定的小寫雙字母代碼，可選國家代碼是ISO-3266指定的大寫雙字母代碼。 例如，美國英語的地區設定字串為`en-US`。
