---
description: 獲取指定公司的活動發佈上下文清單。 如果至少有一個為上下文定義的活動伺服器，則發佈上下文被視為活動。
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 10%

---


# getActivePublishContext{#getactivepublishcontext}

獲取指定公司的活動發佈上下文清單。 如果至少有一個為上下文定義的活動伺服器，則發佈上下文被視為活動。

語法

## 授權用戶類型{#section-eb22397744434dfe92a59ffa2883c2e7}

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
| `*`contextArray`*` | `types:StringArray` | 是 | 作用中發佈上下文的陣列，其中可能包含來自「發佈上下文」的零個或多個值。 |

