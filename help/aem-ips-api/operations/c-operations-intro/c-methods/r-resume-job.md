---
description: 重新啟動暫停的作業。
solution: Experience Manager
title: 恢復作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 17%

---

# 恢復作業{#resumejob}

重新啟動暫停的作業。

語法

## 授權用戶類型 {#section-eab49f4b6d1041179000326a10fee889}

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
| 公司句柄 | `xsd:string` | 是 | 包含要重新啟動的作業的公司的句柄。 |
| 作業句柄 | `xsd:string` | 是 | 暫停作業的句柄。 |

**輸出(resumeJobReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-d0524e031f1f43d89430eade19526162}

此代碼示例將重新啟動暫停的作業。

**請求**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**回答**

無。
