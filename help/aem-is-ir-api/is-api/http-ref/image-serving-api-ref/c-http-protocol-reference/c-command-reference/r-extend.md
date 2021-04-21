---
description: 延伸圖層。 為圖層添加邊界或裁切圖層矩形。
solution: Experience Manager
title: 延伸
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---


# extend{#extend}

延伸圖層。 為圖層添加邊界或裁切圖層矩形。

`extend= *`左`*, *``*, *``*, *`側`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 左、上、下、右</span></span> </p></td> 
  <td class="stentry"> <p>要添加到（如果值為負，則從中移除）圖層的左邊、上邊、右邊和下邊(int、int、int、int)的像素數。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>要添加到（如果值為負，則從中刪除）層直接的左邊、上邊、右邊和下邊的空間量，表示為相對於原始層直接（實數、實數、實數、實數）的標準化量。 </p></td> 
 </tr> 
</table>

`extend=` 會在影像遭到裁 ** 切( `crop=`)後套用至圖層，而且所有圖層變形(包括 `rotate=`在內)都已套用。

擴展區域填充`bgColor=` ，或者，如果未指定，則保持透明。

`extendN=`的引數值在應用層變換後相對於層直的大小進行標準化，包括`rotate=`。

## 屬性 {#section-8fc94de871f841f3bf5e1df135972ca9}

層屬性。 如果`layer=comp`，則套用至層0。 被效果圖層忽略。

## 預設 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`，以保持圖層矩形不變。

## 範例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**裁切影像，然後新增5像素寬的紅色邊框：**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**將影像縮放為200像素寬，並將標題文字加入影像上方30像素的邊界。**

請注意，合成影像的高度會依影像的長寬比而有所不同。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 另請參閱 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , color= [, ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)size=origin= [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b),  [clip ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138) [Path=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
