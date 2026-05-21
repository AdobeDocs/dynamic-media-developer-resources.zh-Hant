---
description: 取得指定公司的作用中發佈內容清單。 如果內容至少定義了一個作用中的伺服器，則發佈內容會被視為作用中。
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
TQID: 'https://experienceleague.adobe.com/g337PVX5asvB-o-VQL0XA5XSrgQ0c2vx0xC4-93Dm8E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 11%

---

# getActivePublishContext{#getactivepublishcontext}

取得指定公司的作用中發佈內容清單。 如果內容至少定義了一個作用中的伺服器，則發佈內容會被視為作用中。

語法

## 授權的使用者型別 {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-a4be4024e55c472fa6728faec9c5e048}

**輸入(getActivePublishContextsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 查詢使用中發佈內容之公司的控制代碼 |

**輸出(getActivePublishContextsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| contextArray | `types:StringArray` | 是 | 作用中發佈內容的陣列，其中可能包括來自發佈內容的零個或多個值。 |
