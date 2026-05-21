---
description: 從標籤欄位的字典中移除標籤欄位值。
solution: Experience Manager
title: deleteTagFieldValue
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
TQID: 'https://experienceleague.adobe.com/SRTriQHWMLXJtkGeS-sCDZE3-1bu1TKNkKjxgESYOi4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 11%

---

# deleteTagFieldValue{#deletetagfieldvalues}

從標籤欄位的字典中移除標籤欄位值。

## 授權的使用者型別 {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-5db64a6ae238426395bc760b83587260}

**輸入(deleteTagFieldValuesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含標籤欄位之公司的控制代碼。 |
| fieldHandle | `xsd:string` | 是 | 要修改之標籤欄位的控點。 |
| valueArray | `types:StringArray` | 是 | 要從欄位字典中刪除的標籤值陣列。 |

**輸出(deleteTagFieldValuesParam)**

IPS API未傳回此作業的回應。

## 範例 {#section-92f9e575a6da491caa09e264b4d6ee55}

**要求**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**回應**

無。
