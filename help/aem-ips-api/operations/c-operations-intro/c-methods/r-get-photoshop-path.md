---
description: 傳回包含命名Photoshop路徑的四邊形座標。
seo-description: 傳回包含命名Photoshop路徑的四邊形座標。
seo-title: getPhotoshopPath
solution: Experience Manager
title: getPhotoshopPath
topic: Dynamic Media Image Production System API
uuid: e3ed4888-18db-40bc-a1db-f44a342d0293
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 17%

---


# getPhotoshopPath{#getphotoshoppath}

傳回包含命名Photoshop路徑的四邊形座標。

語法

## 授權用戶類型{#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## 參數 {#section-ebffe496284c4ced9f329f78127be199}

**輸入(getPhotoshopPathParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 使用您要使用的影像處理公司。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 處理影像資產。 |
| `*`pathName`*` | `xsd:string` | 是 | 您要傳回的Photoshop路徑名稱。 |

**輸出(getPhotoshopPathReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`perspectiveQuad`*` | `types:PerspectiveQuad` | 是 | 根據路徑傳回影像座標。 請參閱[PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)。 |

## 範例 {#section-1f0461cbdc184c8d8925336d5279db47}

**請求**

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**回答**

```java
<getPhotoshopPathReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <perspectiveQuad>
    <x0>932.19</x0>
    <y0>296.592</y0>
    <x1>968.769</x1>
    <y1>320.16</y1>
    <x2>1119.56</x2>
    <y2>1200.0</y2>
    <x3>900.43</x3>
    <y3>1200.0</y3>
  </perspectiveQuad>
</getPhotoshopPathReturn>
```

>[!MORELIKETHIS]
>
>* [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)

