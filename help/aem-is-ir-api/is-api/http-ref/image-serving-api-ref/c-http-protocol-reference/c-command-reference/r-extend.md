---
description: 延伸圖層。 為圖層添加邊距或裁剪圖層矩形。
solution: Experience Manager
title: 延伸
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# 延伸{#extend}

延伸圖層。 為圖層添加邊距或裁剪圖層矩形。

`extend= *``*, *``*, *``*, *`lefttoprightbottom`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 左，上，下，右</span></span> </p></td> 
  <td class="stentry"> <p>要添加到（如果值為負，則從中刪除）圖層直邊的左邊、上邊、右邊和下邊(int、int、int、int)的像素數。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>要向層直接的左邊、上邊、右邊和下邊添加（如果值為負，則從中刪除）的空間量，表示為相對於原始層直接（實、實、實、實）的歸一化量。 </p></td> 
 </tr> 
</table>

`extend=` 會在影像被裁 ** 切後套用至圖層( `crop=`)，且已套用所有圖層轉 `rotate=`換（包括）。

擴展區域填充`bgColor=`，或者，如果未指定，則保持透明。

在應用了`rotate=`等層轉換後，將相對於層直的大小對`extendN=`的參數值進行標準化。

## 屬性 {#section-8fc94de871f841f3bf5e1df135972ca9}

層屬性。 如果`layer=comp`，則應用於層0。 被效果層忽略。

## 預設 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`，不更改圖層矩形。

## 範例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**裁切影像，然後新增5像素寬的紅色邊框：**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**將影像縮放為200像素寬度，並在影像上方的30像素邊界中新增標題文字。**

請注意，複合影像的高度會根據影像的長寬比而不同。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 另請參閱 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b),  [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
