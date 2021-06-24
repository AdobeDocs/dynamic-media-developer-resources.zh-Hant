---
description: 停止正在執行的作業。
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 20%

---

# stopJob{#stopjob}

停止正在執行的作業。

語法

## 授權的使用者類型 {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-2b64f074e37c4c38849994f3bc65342a}

**輸入(stopJobParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`jobHandle`*` | `xsd:string` | 是 | 處理您要停止的工作。 |

**輸出(stopJobReturn0)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-f7e07fa09ae24dc89685533f20ab3b81}

**請求**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**回答**

無。
