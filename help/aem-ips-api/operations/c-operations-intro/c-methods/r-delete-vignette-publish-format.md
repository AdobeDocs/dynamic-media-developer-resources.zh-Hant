---
description: 刪除暈映發佈格式。
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 13%

---

# deleteVignettePublishFormat{#deletevignettepublishformat}

刪除暈映發佈格式。

## 授權的使用者類型 {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-789625ba29df4b5f880914d4c64f77ce}

**輸入(deleteVignettePublishFormatParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 暈船所屬公司的手柄。 |
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 要刪除的暈映發佈格式的句柄。 |

**輸出(deleteVignettePublishFormatParam)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

此程式碼範例會刪除由其控制代碼指定的暈映發佈格式。

**請求**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**回答**

無。
