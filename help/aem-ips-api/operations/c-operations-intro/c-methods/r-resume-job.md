---
description: 重新啟動已暫停的工作。
seo-description: 重新啟動已暫停的工作。
seo-title: resumeJob
solution: Experience Manager
title: resumeJob
topic: Scene7 Image Production System API
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# resumeJob{#resumejob}

重新啟動已暫停的工作。

語法

## 授權使用者類型 {#section-eab49f4b6d1041179000326a10fee889}

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 包含您要重新啟動之工作之公司的控制代碼。 |
| ` *`jobHandle`*` | `xsd:string` | 是 | 暫停作業的句柄。 |

**輸出(resumeJobReturn)**

IPS API不會傳回此作業的回應。

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
