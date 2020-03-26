---
description: 縮放影像。 相對於全解析度影像，按比例縮放圖層源影像。
seo-description: 縮放影像。 相對於全解析度影像，按比例縮放圖層源影像。
seo-title: scale
solution: Experience Manager
title: scale
topic: Scene7 Image Serving - Image Rendering API
uuid: f5540df8-60d9-4efc-99fe-733cdc8268ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scale{#scale}

縮放影像。 相對於全解析度影像，按比例縮放圖層源影像。

`scale= *`因子`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 因子</span> </p> </td> 
  <td class="stentry"> <p>比例因子（實數，大於0.0）。 </p></td> 
 </tr> 
</table>

No scaling is applied when `scale=1`. *`factor`* 小於1.0的下縮放和大於1.0的放大會放大源影像。

## 屬性 {#section-3c7eb45527394fe79b1ddba6c1fcca09}

來源影像／遮色片屬性。 如果同 `size=` 時為當前層指定，則忽略。 Overrides `res=`. 如果為指定，則應用於層0 `layer=comp`。 如果圖層未與影像或遮色片相關聯，則忽略此點。

## 預設 {#section-26e64904362342a5a62c5f6598f330c4}

如果未指定，則 `res=` 使用。 如果未 `res=` 指定，則不使用縮放來使用影像。

## 另請參閱 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
