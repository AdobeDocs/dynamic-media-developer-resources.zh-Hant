---
description: 刪除暈映發佈格式。
seo-description: 刪除暈映發佈格式。
seo-title: deleteVignettePublishFormat
solution: Experience Manager
title: deleteVignettePublishFormat
topic: Scene7 Image Production System API
uuid: 3c8148d5-dec6-4ffa-8ab8-2cd70811ada6
translation-type: tm+mt
source-git-commit: d3766bba78cd1051538ff6a94f61ba61e989f1a5

---


# deleteVignettePublishFormat{#deletevignettepublishformat}

刪除暈映發佈格式。

## 授權使用者類型 {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-789625ba29df4b5f880914d4c64f77ce}

**輸入(deleteVignettePublishFormatParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 暈映所屬公司的控制代碼。 |
| ` *`vignetteFormatHandle`*` | `xsd:string` | 是 | 要刪除暈映發佈格式的句柄。 |

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
