---
description: 更名資產。
solution: Experience Manager
title: 更名資產
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 7%

---

# 更名資產{#renameasset}

更名資產。

>[!NOTE]
>
>的 `renameFiles` 參數已棄用於以前的版本，並已從中刪除 `renameAsset`。 虛擬檔案路徑被更改以與新資產名稱匹配（保留檔案副檔名），而物理檔案路徑不受影響。 API客戶端在更新到新API版本時需要刪除對此參數的引用。

## 授權用戶類型 {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對資產的讀寫權限。

## 參數 {#section-ef95a994106841e0ab346dd4cf672258}

**輸入(renameAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 資產所屬公司的句柄。 |
| 資產句柄 | `xsd:string` | 是 | 要更名的資產的句柄。 |
| 新名稱 | `xsd:string` | 是 | 資產的新名稱。 |
| validateName | `xsd:boolean` | 是 | 如果 `validateName` 是 `true` 並且資產類型需要唯一的IPS ID，然後檢查新名稱是否具有全局唯一性， `renameAsset` 如果它不是唯一的，則拋出錯誤。 |

**輸出(renameAssetReturn)**

IPS API不會為此操作返迴響應。 請參閱 `<ns1:validateName>` 元素。

## 範例 {#section-a0ddffd62bec42e09069f22ceb486f8a}

此代碼示例更名資產

**請求**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**回答**

無。
