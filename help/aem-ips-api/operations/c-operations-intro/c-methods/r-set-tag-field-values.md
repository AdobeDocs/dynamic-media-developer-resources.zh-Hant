---
description: 設定現有標籤欄位的標籤字典值。
solution: Experience Manager
title: settagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
TQID: 'https://experienceleague.adobe.com/--ArL0CPejqbpJX-G7Z8zdU97WVXXjGfWc74UmOWSV0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 13%

---

# settagFieldValues{#settagfieldvalues}

設定現有標籤欄位的標籤字典值。

語法

## 授權的使用者型別 {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-a05cbee4cb4f44198c414a6b14e69156}

**輸入**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控制代碼。 |
| fieldHandle | `xsd:string` | 是 | 標籤欄位控制代碼。 |
| valueArray | `types:StringArray` | 是 | 取代欄位現有字典的標籤值陣列。 當新值與現有值相符時，會維護資產關聯。 |

**輸出(setTagFieldValuesReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-b11cafd9bed54ab5836c737cc075c918}

**要求**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**回應**

無。
