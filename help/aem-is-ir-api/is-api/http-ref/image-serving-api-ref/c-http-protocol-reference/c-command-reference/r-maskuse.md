---
title: 遮色片使用
description: 影像遮色片使用方式。 指定影像的遮色片或Alpha色版如何用於影像的操作（例如，colorize=）。 當在效果圖層中指定時，它允許將效果套用至父圖層的背景區域或整個父圖層矩形。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# 遮色片使用{#maskuse}

影像遮色片使用方式。 指定影像的遮色片或Alpha色版如何用於影像的操作（例如，colorize=）。 當在效果圖層中指定時，它允許將效果套用至父圖層的背景區域或整個父圖層矩形。

`maskUse=norm|invert|off`

下表說明了`maskUse=`的效果，這取決於與圖層影像關聯的遮色片（Alpha色版）的可用性和型別。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>值</b> </th> 
   <th class="entry"> <b>沒有遮罩</b> </th> 
   <th class="entry"> <b>個未關聯的Alpha （或獨立的遮色片影像）</b> </th> 
   <th class="entry"> <b>個相關（預乘） Alpha</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">折扣</span> </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 在填滿實心黑色的矩形上的影像前景區域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">標準</span> </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 影像的前景區域 </p> </td> 
   <td> <p> 影像或圖層的前景區域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">反轉</span> </p> </td> 
   <td> <p> 隱藏圖層 </p> </td> 
   <td> <p> 影像的背景區域 </p> </td> 
   <td> <p> 影像或圖層以純黑色填滿的背景區域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f36ad1af348e45aeb3eb336544df30b0}

影像或圖層屬性。 套用至圖層0 （若`layer=comp`）。 如果在效果圖層指定，該指令會修改從父圖層繼承的遮色片。

當沒有影像遮色片適用時（以`maskUse=`或`mask=`指定），以文字或純色圖層指定時，`catalog::Mask`的行為未定義且不受支援。

## 預設 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 範例 {#section-daa371e9be5547368ff6772342acba0a}

為影像的背景區域上色；影像前景是由個別的遮色片影像所定義。 如果影像未修改，將彩色化的影像背景分層到最上方即可達到此目的：

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 另請參閱 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ， [遮罩=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
