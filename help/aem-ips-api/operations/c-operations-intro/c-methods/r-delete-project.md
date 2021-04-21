---
description: 從公司刪除專案。 資產和專案之間的連結會中斷，但不會從IPS刪除資產。
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 8%

---


# deleteProject{#deleteproject}

從公司刪除專案。 資產和專案之間的連結會中斷，但不會從IPS刪除資產。

語法

## 授權用戶類型{#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-00d1e00dd5014513a52b4e6b4f61de62}

**輸入(deleteProjectParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | 是 | 與項目關聯的公司名稱。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 要刪除的項目的句柄。 |

**輸出(deleteProjectReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-e38507f1f7ec41b9a625f47390490254}

此程式碼範例會使用公司控制代碼和專案控制代碼，作為傳送至IPS Web services伺服器的deleteProjectParam中的欄位來刪除專案。

**請求**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**回答**

無。
