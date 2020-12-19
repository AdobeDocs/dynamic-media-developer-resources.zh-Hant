---
description: 刪除當前作業或已排程作業。
seo-description: 刪除當前作業或已排程作業。
seo-title: deleteJob
solution: Experience Manager
title: deleteJob
topic: Scene7 Image Production System API
uuid: c1109cae-a3ca-40db-b641-9a6fc116c964
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 12%

---


# deleteJob{#deletejob}

刪除當前作業或已排程作業。

語法

## 授權用戶類型{#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-000c42bc93744b1a8e777f3ec3c272b0}

**輸入(deleteJobParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 工作所屬公司的控制代碼。 |
| ` *`jobHandle`*` | `xsd:string` | 是 | 要刪除的作業的句柄。 |

**輸出**

IPS API不會傳回此作業的回應。

## 範例 {#section-732d21d4dad04337b7a5ae1a0cc00eba}

此代碼示例刪除了正在運行或已計畫在IPS中運行的作業。 它需要一個作業句柄，您必須從另一個操作中獲得該句柄。

**請求**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**回答**

無。
