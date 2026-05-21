---
description: 取得搜尋字串、關鍵字和其他資產相關資訊。 回應包含資產的其他相關資訊。
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
TQID: 'https://experienceleague.adobe.com/5w3SvwJWT7831IVQKCbpy7Tc-zULMfiva8UBuglcX-g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 15%

---

# getSearchStrings{#getsearchstrings}

取得搜尋字串、關鍵字和其他資產相關資訊。 回應包含資產的其他相關資訊。

語法

## 授權的使用者型別 {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-c1efda4bb15349a68b276bafee8c18fd}

**輸入(getSearchStringsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司處理。 |
| assetHandle | `xsd:string` | 是 | 處理資產。 |

**輸出(getSearchStringsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| searchStringArray | `types:SearchStrings` | 是 | 資產搜尋字串的陣列。 |

## 範例 {#section-e1f73bff6e4440c489d59cb9aa5384d8}

此程式碼範例會傳回資產特定搜尋字串。 回應會傳回空白陣列。

**要求**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**回應**

無。
