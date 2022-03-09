---
description: 暫停活動作業。
solution: Experience Manager
title: 暫停作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 19%

---

# 暫停作業{#pausejob}

暫停活動作業。

語法

## 授權用戶類型 {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-7aedb924cf8b4e05a0dc927636d537a0}

**輸入(pauseJobParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 把手交給公司。 |
| 作業句柄 | `xsd:string` | 是 | 處理要暫停的作業。 |

**輸出(PauseJobReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-ee4914f9496f4bd88556728a48fb22c1}

此代碼示例暫停活動作業。

**請求**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**回答**

無。
