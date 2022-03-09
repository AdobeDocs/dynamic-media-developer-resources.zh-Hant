---
description: 停止正在執行的作業。
solution: Experience Manager
title: 停止作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 22%

---

# 停止作業{#stopjob}

停止正在執行的作業。

語法

## 授權用戶類型 {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-2b64f074e37c4c38849994f3bc65342a}

**輸入(stopJobParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司負責。 |
| 作業句柄 | `xsd:string` | 是 | 處理要停止的作業。 |

**輸出(stopJobReturn0)**

IPS API不會為此操作返迴響應。

## 範例 {#section-f7e07fa09ae24dc89685533f20ab3b81}

**請求**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**回答**

無。
