---
description: 傳回給定影像的Photoshop路徑名稱陣列。
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 18%

---

# getPhotoshopPathNames{#getphotoshoppathnames}

傳回給定影像的Photoshop路徑名稱陣列。

語法

## 授權的使用者型別 {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-605a4aab23104489a21f7f7f5849801b}

**輸入(getPhotoshopPathNamesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理包含您要使用之影像的公司。 |
| assetHandle | `xsd:string` | 是 | 處理影像資產。 |

**輸出(getPhotoshopPathNamesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| pathNameArray | `types:StringArray` | 是 | 影像中Photoshop路徑名稱的陣列。 |

## 範例 {#section-6d316f14b4184d42af4ca3f717b042dd}

**要求**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**回應**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```
