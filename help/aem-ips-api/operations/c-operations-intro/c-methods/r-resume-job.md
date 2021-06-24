---
description: 重新啟動暫停的作業。
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 16%

---

# resumeJob{#resumejob}

重新啟動暫停的作業。

語法

## 授權的使用者類型 {#section-eab49f4b6d1041179000326a10fee889}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要重新啟動的作業的公司控制代碼。 |
| `*`jobHandle`*` | `xsd:string` | 是 | 已暫停作業的句柄。 |

**輸出(resumeJobReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-d0524e031f1f43d89430eade19526162}

此程式碼範例會重新啟動暫停的工作。

**請求**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**回答**

無。
