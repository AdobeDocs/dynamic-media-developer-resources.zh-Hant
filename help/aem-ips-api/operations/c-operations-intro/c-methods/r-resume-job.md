---
description: 重新啟動暫停的工作。
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
TQID: 'https://experienceleague.adobe.com/WfYbUF7V5-cFK0wwvjPEAVEQc5SHiDiTqU-yBVaQoKg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 67
ht-degree: 14%

---

# resumeJob{#resumejob}

重新啟動暫停的工作。

語法

## 授權的使用者型別 {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**輸入(resumeJobParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含您要重新啟動之工作的公司的控制代碼。 |
| jobHandle | `xsd:string` | 是 | 暫停工作的控制代碼。 |

**輸出(resumeJobReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-d0524e031f1f43d89430eade19526162}

此程式碼範例會重新啟動暫停的工作。

**要求**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**回應**

無。
