---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 22%

---

# getVignettePublishFormats{#getvignettepublishformats}

語法

## 已授權的使用者類型 {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**輸入(getVignettePublishFormatsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |

**輸出(getVignettePublishFormatsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`vignetteFormatArray`*` | `types:VignettePublishFormatArray` | 是 | 暈映發佈格式陣列。 |

## 範例 {#section-2cc32b27cc6243b7b3e273cc05996226}

此程式碼範例會傳回與特定公司相關聯的兩個暈映發佈格式。 資訊會在陣列中傳回，但會為簡潔而截斷。

**請求**

```java
<getVignettePublishFormatsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
</getVignettePublishFormatsParam>
```

**回答**

```java
<getVignettePublishFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatArray>
      <items>
         <companyHandle>c|21</companyHandle>
         <vignetteFormatHandle>v|21|281</vignetteFormatHandle>
         <name>APIcreateVignettePublishFormat</name>
         ...
      </items>
   </vignetteFormatArray>
</getVignettePublishFormatsReturn>
```
