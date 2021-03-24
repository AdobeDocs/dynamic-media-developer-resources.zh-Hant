---
description: 刪除公司的中繼資料欄位。
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---


# deleteMetadataField{#deletemetadatafield}

刪除公司的中繼資料欄位。

語法

## 授權用戶類型{#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-73f12a30cc4340b6b32dd11effd5195e}

**輸入(deleteMetadataFieldParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要刪除之中繼資料欄位之公司的控制代碼。 |
| `*`fieldHandle`*` | `xsd:string` | 是 | 要刪除的元資料欄位的句柄。 |

**輸出(deleteMetadataFieldParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

此程式碼範例會刪除公司的中繼資料欄位。 它使用公司句柄和元資料句柄作為`deleteMetadataFieldParam`中傳遞到IPS Web伺服器的欄位來執行此操作。

**請求**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**回答**

無。0
