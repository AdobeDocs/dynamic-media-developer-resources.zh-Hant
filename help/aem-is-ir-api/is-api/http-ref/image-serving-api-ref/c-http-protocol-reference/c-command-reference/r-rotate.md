---
description: 旋轉影像。 將影像、文本或實色圖層旋轉指定角度。
solution: Experience Manager
title: 旋轉
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 2%

---

# 旋轉{#rotate}

旋轉影像。 將影像、文本或實色圖層旋轉指定角度。

`rotate= *`角`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 角</span> </p> </td> 
  <td class="stentry"> <p>旋轉角度(度（實數）)。 </p></td> 
 </tr> 
</table>

正角順時針旋轉。 層錨點( `anchor=` 或 `catalog::Anchor`)作為旋轉中心。 根據需要放大層矩形並圍繞旋轉資料進行裝配，以避免裁剪。 在填充圖層的背景區域後應用旋轉 `color=`。 `bgColor=` 可用於在旋轉後將背景顏色添加到邊界矩形。

## 屬性 {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

層命令。 應用於當前圖層，如果 `layer=comp`。 被效果層忽略。

## 預設 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`的雙曲餘切值。

## 範例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

將「銷售中」標籤放置在影像目錄中影像的左上角附近。 標籤影像的大小已對300x300視圖正確，應旋轉30度左轉。 用半不透明的白色填充文本框以增強標籤。

`http:// *`伺服器`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

我們申請 `size=` 層0以設定視圖大小，而不是使用 `wid=` 和 `hei=`。 這允許 `myImageId` 在不更改最終大小時調整大小 `labelImage`。 我們還需要具體說明 `scl=1`，否則，可將複合影像縮放到 `attribute::DefaultPix` （除非設定為0,0）。 `color=` 在旋轉前將半不透明背景色添加到文本框。

兩個圖層的原點都設定在左上角，以達到所需的對齊。 注意，層1的原點應用於 `labelImage`旋轉後的值。

請參閱 [示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 在 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) 的子菜單。

## 另請參閱 {#section-c371ee0845994b7382c02e782d1bc595}

[錨=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) 。 [bg顏色=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)。 [顏色=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
