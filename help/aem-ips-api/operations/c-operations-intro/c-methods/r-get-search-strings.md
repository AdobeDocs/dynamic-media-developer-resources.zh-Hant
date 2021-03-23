---
description: 取得搜尋字串、關鍵字和其他資產相關資訊。 回應包含資產的其他資訊。
seo-description: 取得搜尋字串、關鍵字和其他資產相關資訊。 回應包含資產的其他資訊。
seo-title: getSearchStrings
solution: Experience Manager
title: getSearchStrings
uuid: 9d588d6b-c79c-4531-a2e8-8467254a7985
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 13%

---


# getSearchStrings{#getsearchstrings}

取得搜尋字串、關鍵字和其他資產相關資訊。 回應包含資產的其他資訊。

語法

## 授權用戶類型{#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-c1efda4bb15349a68b276bafee8c18fd}

**輸入(getSearchStringsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司負責。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 處理資產。 |

**輸出(getSearchStringsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | 是 | 資產搜尋字串的陣列。 |

## 範例 {#section-e1f73bff6e4440c489d59cb9aa5384d8}

此程式碼範例會傳回資產特定搜尋字串。 響應返回空陣列。

**請求**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**回答**

無。
