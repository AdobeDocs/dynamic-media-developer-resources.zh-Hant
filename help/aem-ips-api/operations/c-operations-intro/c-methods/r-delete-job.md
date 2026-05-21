---
description: 刪除目前或排程的工作。
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
TQID: 'https://experienceleague.adobe.com/rcnHChrY2u5J1-ipPlJ7JilCfbsTHDNDHhqJlLZuWIQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 11%

---

# deleteJob{#deletejob}

刪除目前或排程的工作。

語法

## 授權的使用者型別 {#section-1b959679dc8147c291126ddf7e061742}

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
| companyHandle | `xsd:string` | 是 | 工作所屬公司的控制代碼。 |
| jobHandle | `xsd:string` | 是 | 要刪除之工作的控制代碼。 |

**輸出**

IPS API未傳回此作業的回應。

## 範例 {#section-732d21d4dad04337b7a5ae1a0cc00eba}

此程式碼範例會刪除正在執行或排程在IPS中執行的工作。 它需要工單控制代碼，您必須從其他作業取得此控制代碼。

**要求**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**回應**

無。
