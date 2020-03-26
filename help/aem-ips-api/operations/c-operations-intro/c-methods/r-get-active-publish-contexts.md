---
description: 獲取指定公司的活動發佈上下文清單。 如果至少有一個為上下文定義的活動伺服器，則發佈上下文被視為活動。
seo-description: 獲取指定公司的活動發佈上下文清單。 如果至少有一個為上下文定義的活動伺服器，則發佈上下文被視為活動。
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
topic: Scene7 Image Production System API
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getActivePublishContext{#getactivepublishcontext}

獲取指定公司的活動發佈上下文清單。 如果至少有一個為上下文定義的活動伺服器，則發佈上下文被視為活動。

語法

## 授權使用者類型 {#section-eb22397744434dfe92a59ffa2883c2e7}

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 要查詢活動發佈上下文的公司的句柄 |

**輸出(getActivePublishContextsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`contextArray`*` | `types:StringArray` | 是 | 作用中發佈上下文的陣列，其中可能包含來自「發佈上下文」的零個或多個值。 |

