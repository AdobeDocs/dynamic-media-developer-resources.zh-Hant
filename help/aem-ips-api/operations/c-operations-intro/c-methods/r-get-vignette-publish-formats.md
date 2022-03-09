---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 24%

---

# getVignettePublishFormats{#getvignettepublishformats}

語法

## 授權用戶類型 {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**輸入(getVignettePublishFormatsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司的把手。 |

**輸出(getVignettePublishFormatsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| vignette格式陣列 | `types:VignettePublishFormatArray` | 是 | 視頻發佈格式的陣列。 |

## 範例 {#section-2cc32b27cc6243b7b3e273cc05996226}

此代碼示例返回與特定公司關聯的兩種視頻發佈格式。 資訊在陣列中返回，該陣列被截斷以便簡化。

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
