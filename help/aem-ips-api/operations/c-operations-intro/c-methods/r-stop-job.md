---
description: 停止正在處理的作業。
seo-description: 停止正在處理的作業。
seo-title: stopJob
solution: Experience Manager
title: stopJob
topic: Scene7 Image Production System API
uuid: 698c1652-5afa-4a2c-819a-1ba6ffc6aacf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 20%

---


# stopJob{#stopjob}

停止正在處理的作業。

語法

## 授權用戶類型{#section-b222f561143747f6ad089aadc0b274d8}

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| ` *`jobHandle`*` | `xsd:string` | 是 | 處理您要停止的工作。 |

**輸出(stopJobReturn0)**

IPS API不會傳回此作業的回應。

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
