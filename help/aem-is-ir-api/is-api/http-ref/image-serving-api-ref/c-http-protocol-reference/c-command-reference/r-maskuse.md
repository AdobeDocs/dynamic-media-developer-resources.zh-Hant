---
description: 影像遮色片的使用。 指定如何使用影像的遮色片或Alpha色版來執行影像上的作業（例如colorize=）。 當在效果圖層中指定時，它允許將效果套用至父圖層的背景區域或整個父圖層矩形。
solution: Experience Manager
title: maskUse
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---


# maskUse{#maskuse}

影像遮色片的使用。 指定如何使用影像的遮色片或Alpha色版來執行影像上的作業（例如colorize=）。 當在效果圖層中指定時，它允許將效果套用至父圖層的背景區域或整個父圖層矩形。

`maskUse=norm|invert|off`

下表說明了`maskUse=`的效果，具體取決於與圖層影像相關聯的遮色片（alpha色版）的可用性和類型。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 值</b> </th> 
   <th class="entry"> <b> 無遮色片</b> </th> 
   <th class="entry"> <b> 未關聯的Alpha（或單獨的遮色片影像）</b> </th> 
   <th class="entry"> <b> 相關（預乘）alpha</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 關閉 </span> </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 填滿純黑的矩形前景影像區域 </p> </td> 
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
   <td> <p> 填滿純黑的影像或圖層的背景區域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f36ad1af348e45aeb3eb336544df30b0}

影像或圖層屬性。 如果`layer=comp`，則套用至層0。 如果在效果圖層中指定，則命令將修改從父層繼承的蒙版。

當沒有影像遮色片可用時（以`mask=`或`catalog::Mask`指定），如果與文字或純色圖層一起指定，則`maskUse=`的行為是未定義的，且不支援。

## 預設 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 範例 {#section-daa371e9be5547368ff6772342acba0a}

為影像的背景區域上色；影像前景由單獨的遮色片影像定義。 若未修改的影像，則將彩色化的影像背景層疊在上方，以達到此目的：

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 另請參閱 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ，遮 [色片=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
