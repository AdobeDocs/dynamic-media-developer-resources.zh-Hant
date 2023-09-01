---
title: 旋轉
description: 旋轉影像。 將影像、文字或純色圖層旋轉指定的角度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 2%

---

# 旋轉{#rotate}

旋轉影像。 將影像、文字或純色圖層旋轉指定的角度。

`rotate= *`角度`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 角度</span> </p> </td> 
  <td class="stentry"> <p>以度（實數）為單位的旋轉角度。 </p></td> 
 </tr> 
</table>

正角度會順時針旋轉。 圖層錨點( `anchor=` 或 `catalog::Anchor`)作為旋轉中心。 圖層矩形會放大，並視需要配合旋轉後的資料，以避免裁切。 在填滿圖層的背景區域後，會套用旋轉 `color=`. 修飾元 `bgColor=` 可用來在旋轉後新增背景顏色至邊界矩形。

## 屬性 {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

圖層指令。 套用至目前的圖層，或套用至圖層0，如果 `layer=comp`. 被效果圖層忽略。

## 預設 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`，表示無旋轉。

## 範例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

在影像目錄的影像左上角附近放置「銷售中」標籤。 標籤影像已針對300x300檢視正確調整大小，應該向左旋轉30°。 若要增強標籤，請以白色、半不透明的顏色填滿文字方塊。

`http:// *`伺服器`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

套用 `size=` 至圖層0以設定檢視大小，而非使用 `wid=` 和 `hei=`. 此方法允許 `myImageId` 以調整大小，而不變更最終大小 `labelImage`. 此外，請指定 `scl=1`，否則複合影像可能會縮放至 `attribute::DefaultPix` （除非已設為0,0）。 修飾元 `color=` 在旋轉之前，將半不透明的背景顏色加入文字方塊。

兩個圖層的原點都會設定為左上角，以達成所要的對齊。 圖層1的原點套用至 `labelImage`在它旋轉之後。

另請參閱 [範例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 在 [範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) 例如旋轉文字的範例。

## 另請參閱 {#section-c371ee0845994b7382c02e782d1bc595}

[錨點=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ， [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)， [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
