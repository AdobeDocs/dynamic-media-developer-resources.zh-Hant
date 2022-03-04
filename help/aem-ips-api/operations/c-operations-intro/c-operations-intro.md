---
description: 描述由IPS Web服務API處理的常見操作參數。
solution: Experience Manager
title: 操作方法
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# 操作方法{#operations-methods}

本節介紹由IPS Web服務API處理的常見操作參數。

有關每個操作參數的完整說明，請參見 [操作參數](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md)。

## 句柄：關於 {#section-094ce1afa6244fa5b2c762f44ffdca1c}

處理某些API操作返回的引用IPS對象。 也可以將句柄作為參數傳遞給後續操作調用。 句柄是字串資料類型( `xsd:string`)。

句柄僅用於單個應用程式會話期間。 此外，您應使句柄保持持久性，因為它們的格式可以在IPS版本之間更改。 在編寫互動式應用程式時，您會實施會話超時並放棄會話之間的所有句柄，尤其是在IPS升級後。 編寫非互動式應用程式時，每次運行應用程式時都調用相應的操作以檢索句柄。 以下Java/Axis2代碼示例顯示代碼執行不正確且正確：

**句柄代碼不正確**

此代碼示例不正確，因為它包含公司句柄的硬編碼值(555)。

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**正確的句柄代碼**

此代碼示例正確，因為它調用 `getCompanyInfo` 返回有效句柄。 它不依賴於硬編碼值。 使用此方法或其它等效IPS API返回所需句柄。

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## 常用句柄類型 {#section-e683ac8283284f9688e63f51a494f7a0}

**公司句柄**

大多數操作都要求您通過傳遞 `companyHandle` 的下界。 公司句柄是某些操作(如 `getCompanyInfo`。 `addCompany`, `getCompanyMembership`。

**userHandle**

的 `userHandle` 參數是針對特定用戶的操作的可選參數。 預設情況下，這些操作針對的是調用用戶（其憑據已傳入以進行身份驗證的用戶）。 但是，具有適當權限的管理員用戶可以指定其他用戶。 例如， `setPassword` 操作通常設定已驗證用戶的密碼，但管理員可以使用 `userHandle` 參數，以設定其他用戶的口令。

對於需要公司上下文的操作(使用 `companyHandle` 參數)，已驗證的用戶和目標用戶都必須是指定公司的成員。 對於不需要公司上下文的操作，已驗證的用戶和目標用戶必須都是至少一個公用公司的成員。

以下操作可以檢索用戶句柄：

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle和accessGroupHandle**

預設情況下，需要訪問權限（讀、寫、刪除）的操作在調用用戶的權限上下文中進行。 某些操作允許您使用 `accessUserHandle` 或 `accessGroupHandle` 的下界。 的 `accessUserHandle` 參數允許管理員模擬其他用戶。 的 `accessGroupHandle` 參數允許調用方在特定用戶組的上下文中操作。

**responseFieldArray和excludeFieldArray**

某些操作允許調用方限制響應中包含哪些欄位。 限制欄位有助於減少處理請求所需的時間和記憶體並減小響應資料的大小。 調用方可以通過傳遞 `responseFieldArray` 參數，或通過枚舉的清單列出排除的欄位 `excludeFieldArray` 的下界。

兩者 `responseFieldArray` 和 `excludeFieldArray` 使用由 `/`。 例如，要指定 `searchAssets` 僅返回每個資產的名稱、上次修改日期和元資料，請參閱以下內容：

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

同樣，要返回所有欄位（權限除外）:

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

請注意，節點路徑與返回節點根相對。 如果指定不包含任何子元素的複雜類型欄位(例如， `assetArray/items/imageInfo`)，則包含其所有子元素。 如果在複雜類型欄位中指定一個或多個子元素(例如， `assetArray/items/imageInfo/originalPath`)，則只包括這些子元素。

如果不包括 `responseFieldArray` 或 `excludeFieldArray` 在請求中，將返回所有欄位。

**地區設定**

自IPS 4.0以來，IPS API支援通過傳遞 `authHeader` 區域設定參數。 如果區域設定參數不存在，則HTTP標頭 `Accept-Language` 的子菜單。 如果此標頭不存在，則使用IPS伺服器的預設區域設定。

某些操作還採用顯式語言環境參數，這些參數可能與操作語言環境上下文不同。 例如， `submitJob` 操作 `locale` 設定用於作業日誌記錄和電子郵件通知的區域設定的參數。

區域設定參數使用格式 `<language_code>[-<country_code>]`

如果語言代碼是ISO-639指定的小寫雙字母代碼，而可選國家代碼是ISO-3266指定的大寫雙字母代碼。 例如，US English的區域設定字串為 `en-US`。
