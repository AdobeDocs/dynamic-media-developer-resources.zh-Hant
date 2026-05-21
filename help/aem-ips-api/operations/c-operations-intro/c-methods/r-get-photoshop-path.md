---
description: 傳回包含已命名Photoshop路徑的四邊形座標。
solution: Experience Manager
title: getPhotoshopPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 46d88547-bb60-4370-9c79-bd281b40ba28
TQID: 'https://experienceleague.adobe.com/oYuZ7LC10b-3r3VvI-Kg4tlD7rMtshcswi3hctp6aUM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 17%

---

# getPhotoshopPath{#getphotoshoppath}

傳回包含已命名Photoshop路徑的四邊形座標。

語法

## 授權的使用者型別 {#section-c417a287612847cb98dd0aa9c67fd78a}

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
| companyHandle | `xsd:string` | 是 | 使用您要處理的影像處理公司。 |
| assetHandle | `xsd:string` | 是 | 處理影像資產。 |
| pathName | `xsd:string` | 是 | 您要傳回的Photoshop路徑名稱。 |

**輸出(getPhotoshopPathReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 透視四色 | `types:PerspectiveQuad` | 是 | 根據路徑傳回影像座標。 請參閱[PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204) |

## 範例 {#section-1f0461cbdc184c8d8925336d5279db47}

**要求**

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**回應**

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
>* [透視](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)
