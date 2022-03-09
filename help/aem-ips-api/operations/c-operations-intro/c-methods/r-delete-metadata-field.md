---
description: 刪除公司的元資料欄位。
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 11%

---

# deleteMetadataField{#deletemetadatafield}

刪除公司的元資料欄位。

語法

## 授權用戶類型 {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-73f12a30cc4340b6b32dd11effd5195e}

**輸入(deleteMetadataFieldParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 包含要刪除的元資料欄位的公司的句柄。 |
| 欄位句柄 | `xsd:string` | 是 | 要刪除的元資料欄位的句柄。 |

**輸出(deleteMetadataFieldParam)**

IPS API不會為此操作返迴響應。

## 範例 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

此代碼示例刪除公司的元資料欄位。 它將公司句柄和元資料句柄用作 `deleteMetadataFieldParam` 傳入IPS Web服務伺服器以執行此操作。

**請求**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**回答**

無。0
