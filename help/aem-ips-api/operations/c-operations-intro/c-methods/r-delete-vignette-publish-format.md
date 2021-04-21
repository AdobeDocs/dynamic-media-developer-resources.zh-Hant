---
description: 刪除暈映發佈格式。
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 13%

---


# deleteVignettePublishFormat{#deletevignettepublishformat}

刪除暈映發佈格式。

## 授權用戶類型{#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-789625ba29df4b5f880914d4c64f77ce}

**輸入(deleteVignettePublishFormatParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 暈映所屬公司的控制代碼。 |
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 要刪除暈映發佈格式的句柄。 |

**輸出(deleteVignettePublishFormatParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

此程式碼範例會刪除其控制代碼所指定的暈映發佈格式。

**請求**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**回答**

無。
