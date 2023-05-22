---
description: 縮放影像。 相對於全解析度影像按因子縮放圖層源影像。
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 4%

---

# scale{#scale}

縮放影像。 相對於全解析度影像按因子縮放圖層源影像。

`scale= *`因子`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 因子</span> </p> </td> 
  <td class="stentry"> <p>比例因子（實數，大於0.0）。 </p></td> 
 </tr> 
</table>

在 `scale=1`。 *`factor`* 小於1.0的下縮放和大於1.0的放大源影像。

## 屬性 {#section-3c7eb45527394fe79b1ddba6c1fcca09}

源影像/蒙版屬性。 如果忽略 `size=` 也為當前層指定。 覆蓋 `res=`。 如果為指定，則應用於層0 `layer=comp`。 如果圖層未與影像或蒙版關聯，則忽略。

## 預設 {#section-26e64904362342a5a62c5f6598f330c4}

如果未指定， `res=` 的子菜單。 如果 `res=` 未指定，則使用影像時不進行縮放。

## 另請參閱 {#section-61a11f30d37341d58c10df759bfff951}

[雷斯=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) 。 [大小=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
