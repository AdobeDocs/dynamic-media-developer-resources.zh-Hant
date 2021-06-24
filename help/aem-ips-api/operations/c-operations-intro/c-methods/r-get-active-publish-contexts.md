---
description: 獲取指定公司的活動發佈上下文的清單。 如果至少為上下文定義了一個活動伺服器，則將發佈上下文視為活動。
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 10%

---

# getActivePublishContext{#getactivepublishcontext}

獲取指定公司的活動發佈上下文的清單。 如果至少為上下文定義了一個活動伺服器，則將發佈上下文視為活動。

語法

## 授權的使用者類型 {#section-eb22397744434dfe92a59ffa2883c2e7}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 要查詢活動發佈上下文的公司的句柄 |

**輸出(getActivePublishContextsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | 是 | 作用中發佈內容的陣列，其中可能包含來自發佈內容的零個或多個值。 |
