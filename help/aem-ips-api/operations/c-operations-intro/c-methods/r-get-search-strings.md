---
description: 取得資產的搜尋字串、關鍵字及其他資訊。 回應包含有關資產的其他資訊。
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 17%

---

# getSearchStrings{#getsearchstrings}

取得資產的搜尋字串、關鍵字及其他資訊。 回應包含有關資產的其他資訊。

語法

## 授權的使用者類型 {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-c1efda4bb15349a68b276bafee8c18fd}

**輸入(getSearchStringsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司處理。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 處理資產。 |

**輸出(getSearchStringsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | 是 | 資產搜尋字串的陣列。 |

## 範例 {#section-e1f73bff6e4440c489d59cb9aa5384d8}

此程式碼範例會傳回資產特定搜尋字串。 回應會傳回空白陣列。

**請求**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**回答**

無。
