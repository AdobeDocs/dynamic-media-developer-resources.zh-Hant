---
description: 傳回指定影像的Photoshop路徑名稱陣列。
seo-description: 傳回指定影像的Photoshop路徑名稱陣列。
seo-title: getPhotoshopPathNames
solution: Experience Manager
title: getPhotoshopPathNames
topic: Scene7 Image Production System API
uuid: d3f1dea5-393b-498e-963d-37a4e38068a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 17%

---


# getPhotoshopPathNames{#getphotoshoppathnames}

傳回指定影像的Photoshop路徑名稱陣列。

語法

## 授權用戶類型{#section-baa0fd4b92bc4ad89809efd659b3a629}

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 包含您要使用之影像的公司控制代碼。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 處理影像資產。 |

**輸出(getPhotoshopPathNamesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`pathNameArray`*` | `types:StringArray` | 是 | 影像中的Photoshop路徑名稱陣列。 |

## 範例 {#section-6d316f14b4184d42af4ca3f717b042dd}

**請求**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**回答**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```

