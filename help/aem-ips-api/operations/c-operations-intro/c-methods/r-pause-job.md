---
description: 暫停作用中的工作。
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
TQID: 'https://experienceleague.adobe.com/7zMJW9fm8DiAPrO5cCDl87FhFMbgpw5NxoBHmIfEBog'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 16%

---

# pauseJob{#pausejob}

暫停作用中的工作。

語法

## 授權的使用者型別 {#section-f2bf306ab4574871bd21f9f7dd681033}

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
| companyHandle | `xsd:string` | 是 | 公司處理。 |
| jobHandle | `xsd:string` | 是 | 處理您要暫停的工作。 |

**輸出(PauseJobReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-ee4914f9496f4bd88556728a48fb22c1}

此程式碼範例會暫停作用中的工作。

**要求**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**回應**

無。

