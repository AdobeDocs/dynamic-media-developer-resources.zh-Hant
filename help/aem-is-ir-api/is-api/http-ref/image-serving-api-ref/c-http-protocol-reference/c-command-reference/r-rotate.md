---
description: 旋轉影像。 將影像、文字或純色圖層旋轉指定的角度。
seo-description: 旋轉影像。 將影像、文字或純色圖層旋轉指定的角度。
seo-title: 旋轉
solution: Experience Manager
title: 旋轉
topic: Scene7 Image Serving - Image Rendering API
uuid: 160d3c4b-3871-43bd-a17d-96198c7ea839
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# rotate{#rotate}

旋轉影像。 將影像、文字或純色圖層旋轉指定的角度。

`rotate= *`角度`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 角度</span> </p> </td> 
  <td class="stentry"> <p>旋轉角度（以度為單位）。 </p></td> 
 </tr> 
</table>

正角度順時針旋轉。 圖層錨點( `anchor=` 或 `catalog::Anchor`)用作旋轉中心。 圖層矩形被放大，並視需要圍繞旋轉的資料進行配合，以避免裁切。 在將圖層的背景區域填入後，會套用旋轉 `color=`。 `bgColor=` 可用於在旋轉後將背景顏色添加到邊界矩形。

## 屬性 {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

圖層命令。 應用於當前層，或應用於層0（如果） `layer=comp`。 被效果圖層忽略。

## 預設 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`，以禁止旋轉。

## 範例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

將「銷售中」標籤置於影像目錄中影像的左上角附近。 標籤影像的大小已正確，適用於300x300檢視，且應該向左旋轉30度。 用白色半不透明顏色填入文字方塊，以增強標籤。

`http:// *`伺服器`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

我們會 `size=` 套用至圖層0以設定檢視大小，而非使用 `wid=` 和 `hei=`。 這可讓 `myImageId` 您在不變更最終大小時調整大小 `labelImage`。 我們還需要指 `scl=1`定，否則合成影像可能會縮放 `attribute::DefaultPix` 為（除非設定為0,0）。 `color=` 在旋轉之前，將半不透明的背景顏色添加到文本框。

兩個圖層的原點都設定在左上角，以達到所需的對齊方式。 請注意，圖層1的原點在旋轉 `labelImage`後會套用至。

如需 [旋轉文字的范](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 例 [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) ，請參閱範本中的範例A。

## 另請參閱 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
