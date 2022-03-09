---
description: 獲取有關資產的搜索字串、關鍵字和其他資訊。 響應包含有關資產的其他資訊。
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 17%

---

# getSearchStrings{#getsearchstrings}

獲取有關資產的搜索字串、關鍵字和其他資訊。 響應包含有關資產的其他資訊。

語法

## 授權用戶類型 {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-c1efda4bb15349a68b276bafee8c18fd}

**Input(getSearchStringsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 把手交給公司。 |
| 資產句柄 | `xsd:string` | 是 | 處理資產。 |

**輸出(getSearchStringsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| searchStringArray | `types:SearchStrings` | 是 | 資產搜索字串的陣列。 |

## 範例 {#section-e1f73bff6e4440c489d59cb9aa5384d8}

此代碼示例返回特定於資產的搜索字串。 響應返回空陣列。

**請求**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**回答**

無。
