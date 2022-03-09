---
description: 刪除當前作業或計畫作業。
solution: Experience Manager
title: 刪除作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 13%

---

# 刪除作業{#deletejob}

刪除當前作業或計畫作業。

語法

## 授權用戶類型 {#section-1b959679dc8147c291126ddf7e061742}

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
| 公司句柄 | `xsd:string` | 是 | 作業所屬公司的句柄。 |
| 作業句柄 | `xsd:string` | 是 | 要刪除的作業的句柄。 |

**輸出**

IPS API不會為此操作返迴響應。

## 範例 {#section-732d21d4dad04337b7a5ae1a0cc00eba}

此代碼示例刪除正在運行或計畫在IPS中運行的作業。 它需要一個任務句柄，您必須從另一個工序中獲得該句柄。

**請求**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**回答**

無。
