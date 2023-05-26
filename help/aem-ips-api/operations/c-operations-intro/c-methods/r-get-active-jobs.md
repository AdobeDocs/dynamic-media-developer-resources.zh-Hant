---
description: 取得所有目前作用中的工作。
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 16%

---

# getActiveJobs{#getactivejobs}

取得所有目前作用中的工作。

語法

## 授權的使用者型別 {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**輸入(getActiveJobsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 否 | 公司的控制代碼。 |
| jobHandle | `xsd:string` | 否 | 工作的控制代碼。 |
| 原始名稱 | `xsd:string` | 否 | 原始工作名稱。 |

**輸出(getActiveJobsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| jobArray | `xsd:string` | 是 | 作用中工作的陣列。 |

## 範例 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

此程式碼範例會傳回公司在IPS中執行的所有作用中工作。 在此情況下，回應是不尋常的，因為IPS排程協調器已停用，而且沒有執行中的作用中工作。 在正常情況下，回應會傳回許多作用中的工作。

**請求**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**回答**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```
