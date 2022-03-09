---
description: 返回封閉指定Photoshop路徑的四邊形的坐標。
solution: Experience Manager
title: getPhotoshopPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 46d88547-bb60-4370-9c79-bd281b40ba28
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 19%

---

# getPhotoshopPath{#getphotoshoppath}

返回封閉指定Photoshop路徑的四邊形的坐標。

語法

## 授權用戶類型 {#section-c417a287612847cb98dd0aa9c67fd78a}

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
| 公司句柄 | `xsd:string` | 是 | 使用要使用的映像處理公司。 |
| 資產句柄 | `xsd:string` | 是 | 處理影像資產。 |
| 路徑名 | `xsd:string` | 是 | 要返回的Photoshop路徑的名稱。 |

**輸出(getPhotoshopPathReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 透視四 | `types:PerspectiveQuad` | 是 | 根據路徑返回影像坐標。 請參閱 [透視四](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)。 |

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
>* [透視四](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)

