---
description: 影像掩碼用法。 指定影像的蒙版或Alpha通道如何用於對影像進行操作（例如，colorize=）。 當在效果圖層中指定時，它允許將效果應用於父圖層的背景區域或整個父圖層矩形。
solution: Experience Manager
title: 掩碼使用
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# 掩碼使用{#maskuse}

影像掩碼用法。 指定影像的蒙版或Alpha通道如何用於對影像進行操作（例如，colorize=）。 當在效果圖層中指定時，它允許將效果應用於父圖層的背景區域或整個父圖層矩形。

`maskUse=norm|invert|off`

下表說明了 `maskUse=` 取決於與圖層影像關聯的掩碼（Alpha通道）的可用性和類型。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 值</b> </th> 
   <th class="entry"> <b> 無掩碼</b> </th> 
   <th class="entry"> <b> 未關聯的Alpha（或單獨的蒙版影像）</b> </th> 
   <th class="entry"> <b> 關聯（預乘）α</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 關閉 </span> </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 實心黑色填充的矩形上的影像前景區域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 范數 </span> </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 影像的前景區域 </p> </td> 
   <td> <p> 影像或圖層的前景區域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 反 </span> </p> </td> 
   <td> <p> 隱藏層 </p> </td> 
   <td> <p> 影像背景區域 </p> </td> 
   <td> <p> 用實心黑色填充的影像或圖層的背景區域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f36ad1af348e45aeb3eb336544df30b0}

影像或圖層屬性。 如果為 `layer=comp`。 如果在效果層中指定，則此命令將修改從父層繼承的蒙版。

的行為 `maskUse=` 未定義，如果不適用影像蒙版，則不支援在文本或實色圖層中指定（使用指定） `mask=` 或 `catalog::Mask`)。

## 預設 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 範例 {#section-daa371e9be5547368ff6772342acba0a}

對影像的背景區域著色；影像前景由單獨的蒙版影像定義。 如果未修改的影像：

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 另請參閱 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[顏色=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) 。 [掩碼=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
