---
description: 重新命名專案。
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
TQID: 'https://experienceleague.adobe.com/FjPL1Xn4QAYYCdyeYKA1MiQVay988g-sbuiHpazhcMM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 21%

---

# renameProject{#renameproject}

重新命名專案。

語法

## 授權的使用者型別 {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-43ccd77648784be4a259a723c3e1db40}

**輸入(renameProjectParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyName | `xsd:string` | 是 | 處理您要重新命名之專案的公司。 |
| projectHandle | `xsd:string` | 是 | 處理專案。 |
| projectName | `xsd:string` | 是 | 新專案名稱。 |

**輸出(renameProjectParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| projectHandle | `xsd:string` | 是 | 已重新命名專案的控點。 |

## 範例 {#section-a0a06d9244774795b695a10b92b2a5e7}

此程式碼範例會重新命名專案並傳回專案控制代碼。

**要求**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**回應**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```
