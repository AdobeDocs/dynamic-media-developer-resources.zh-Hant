---
description: 影像遮色片使用方式。 指定如何使用影像的遮色片或Alpha通道來對影像執行操作（例如colorize=）。 在效果層中指定時，它允許將效果應用到父層的背景區域或整個父層矩形。
solution: Experience Manager
title: maskUse
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# maskUse{#maskuse}

影像遮色片使用方式。 指定如何使用影像的遮色片或Alpha通道來對影像執行操作（例如colorize=）。 在效果層中指定時，它允許將效果應用到父層的背景區域或整個父層矩形。

`maskUse=norm|invert|off`

下表說明了`maskUse=`的影響，具體取決於與圖層影像相關聯的掩模（Alpha通道）的可用性和類型。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 值</b> </th> 
   <th class="entry"> <b> 無遮罩</b> </th> 
   <th class="entry"> <b> 未關聯的Alpha（或單獨的蒙版影像）</b> </th> 
   <th class="entry"> <b> 關聯（預先乘上）alpha</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 關閉 </span> </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 用實心黑色填充的矩形上的影像前景區域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 規範  </span> </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 影像的前景區域 </p> </td> 
   <td> <p> 影像或圖層的前景區域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 反轉  </span> </p> </td> 
   <td> <p> 隱藏圖層 </p> </td> 
   <td> <p> 影像的背景區域 </p> </td> 
   <td> <p> 用實心黑色填充的影像或圖層的背景區域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f36ad1af348e45aeb3eb336544df30b0}

影像或圖層屬性。 如果`layer=comp`，則應用於層0。 如果在效果層中指定，則命令將修改從父層繼承的掩碼。

未定義`maskUse=`的行為，當沒有影像遮色片適用時（以`mask=`或`catalog::Mask`指定），則不支援以文字或實色層指定。

## 預設 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 範例 {#section-daa371e9be5547368ff6772342acba0a}

將影像的背景區域著色；影像前景由單獨的蒙版影像定義。 這是通過在未修改的影像上將彩色影像背景分層來實現的：

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 另請參閱 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
