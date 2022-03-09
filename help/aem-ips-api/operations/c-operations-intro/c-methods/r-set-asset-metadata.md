---
description: 設定資產的元資料值。 與元資料更新陣列一起使用，以在批處理中設定值。
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 10%

---

# setAssetMetadata{#setassetmetadata}

設定資產的元資料值。 與元資料更新陣列一起使用，以在批處理中設定值。

語法

## 授權用戶類型 {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對資產的讀取權限。

## 參數 {#section-bcdcff30905e444388811e897b2824bd}

**輸入(setAssetMetadataParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 要更新資產的公司的句柄。 |
| 資產句柄 | `xsd:string` | 是 | 資產的句柄。 |
| 更新陣列 | `types:MetadataUpdateArray` | 是 | 元資料更新陣列中的更新。 |

**輸出(setAssetMetadataReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-1ab412e7ee1d4d6d8469b0b403598c42}

此代碼示例使用元資料更新陣列來設定指定資產的元資料。

**請求**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**回答**

無。
