---
description: 暫停活動作業。
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 18%

---

# pauseJob{#pausejob}

暫停活動作業。

語法

## 授權的使用者類型 {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-7aedb924cf8b4e05a0dc927636d537a0}

**輸入(pauseJobParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司處理。 |
| `*`jobHandle`*` | `xsd:string` | 是 | 處理要暫停的作業。 |

**輸出(PauseJobReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-ee4914f9496f4bd88556728a48fb22c1}

此代碼示例暫停活動作業。

**請求**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**回答**

無。
