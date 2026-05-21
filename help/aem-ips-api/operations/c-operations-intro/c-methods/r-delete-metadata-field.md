---
description: 刪除公司的中繼資料欄位。
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
TQID: 'https://experienceleague.adobe.com/GnKkb-vTCdD5PwU111sxefzxR7FN74hk3i66c3gcH9I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 9%

---

# deleteMetadataField{#deletemetadatafield}

刪除公司的中繼資料欄位。

語法

## 授權的使用者型別 {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-73f12a30cc4340b6b32dd11effd5195e}

**輸入(deleteMetadataFieldParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要刪除之中繼資料欄位的公司的控制代碼。 |
| fieldHandle | `xsd:string` | 是 | 要刪除的中繼資料欄位的控制代碼。 |

**輸出(deleteMetadataFieldParam)**

IPS API未傳回此作業的回應。

## 範例 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

此程式碼範例會刪除公司的中繼資料欄位。 它使用公司控制代碼和中繼資料控制代碼作為傳遞至IPS Web服務伺服器的`deleteMetadataFieldParam`中的欄位，以執行此動作。

**要求**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**回應**

無。0
