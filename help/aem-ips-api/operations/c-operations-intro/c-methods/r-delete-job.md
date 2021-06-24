---
description: 刪除當前或計畫的作業。
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 12%

---

# deleteJob{#deletejob}

刪除當前或計畫的作業。

語法

## 授權的使用者類型 {#section-1b959679dc8147c291126ddf7e061742}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 工作所屬公司的控制代碼。 |
| `*`jobHandle`*` | `xsd:string` | 是 | 要刪除的作業的句柄。 |

**輸出**

IPS API不會針對此操作傳回回應。

## 範例 {#section-732d21d4dad04337b7a5ae1a0cc00eba}

此程式碼範例會刪除正在執行或排程在IPS中執行的作業。 它需要作業句柄，您必須從其他操作中獲取該句柄。

**請求**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**回答**

無。
