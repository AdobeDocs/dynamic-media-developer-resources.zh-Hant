---
description: 暫停活動作業。
seo-description: 暫停活動作業。
seo-title: pauseJob
solution: Experience Manager
title: pauseJob
topic: Scene7 Image Production System API
uuid: baad2ad6-46f5-4133-a6d9-8ffadf990a06
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pauseJob{#pausejob}

暫停活動作業。

語法

## 授權使用者類型 {#section-f2bf306ab4574871bd21f9f7dd681033}

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 為公司負責。 |
| ` *`jobHandle`*` | `xsd:string` | 是 | 處理您要暫停的工作。 |

**輸出(PauseJobReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-ee4914f9496f4bd88556728a48fb22c1}

此程式碼範例會暫停作用中的工作。

**請求**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**回答**

無。
