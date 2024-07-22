---
title: 圖層效果
description: Photoshop樣式圖層陰影和光暈效果是使用特殊子圖層（效果圖層）來實作，這些子圖層可以附加到任何圖層（父圖層），包括layer=0和layer=comp。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 2%

---

# 圖層效果{#layer-effects}

Photoshop樣式圖層陰影和光暈效果是使用特殊子圖層（效果圖層）來實作，這些子圖層可以附加到任何圖層（父圖層），包括layer=0和layer=comp。

雖然效果圖層支援許多標準的影像和圖層屬性及指令，但這些圖層並非一般用途圖層，也不支援獨立的影像或文字資料。

任何數量的圖層效果都可以附加至單一父圖層。

## 內部和外部效果 {#section-2dade7ee98e041d1b4d1725e6f98a515}

*內部效果*&#x200B;會呈現在上層圖層的頂端，而且只會在上層圖層的不透明區域顯示。 *外部效果*&#x200B;會呈現在上層圖層後面（因此它們永遠不會顯示在上層圖層的不透明區域中），而且可以放置在合成畫布的任何位置。 使用`effect=`指令指定正或負效果圖層編號，以選擇內部或外部效果。 `effect=`指令也會控制附加至相同父圖層的多個效果圖層之間的z順序。

## 與上層圖層的關係 {#section-eb8bfc4f754a42fc973b562821d6f2d3}

效果圖層會自動調整大小並定位為與父圖層一致（也就是說，效果圖層會繼承父圖層的`size=`和`origin=`值）。 `pos=`可用來將效果圖層移離上層圖層，這是投影和內陰影效果通常需要的功能。 對於標準圖層`pos=`會指定此圖層原點與圖層0之間的位移，而對於效果圖層`pos=`則會指定效果圖層原點與父圖層之間的位移。

## 支援的命令和屬性 {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

效果圖層接受下列指令和屬性：

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

會忽略效果圖層中包含的所有其他影像和圖層指令。

## 預設效果巨集 {#section-a01e8dcc87c94495b54a6dfb21d2a718}

為了方便使用圖層效果， IS提供兩個具有預設影像目錄`$shadow$`和`$glow$`的巨集，這兩個巨集可提供與Photoshop圖層效果類似的效果圖層屬性預設值。 下表列出應使用哪些效果指令和巨集來實作預設圖層效果。 自然地，可在URL中修改巨集中指定的任何屬性，或可建立其他巨集以實作自訂圖層效果。

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>想要的效果</b> </th> 
   <th class="entry"> <b>命令</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> 陰影 </p> </td> 
   <td> <p> <span class="codeph">效果=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 內陰影 </p> </td> 
   <td> <p> <span class="codeph">效果=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 外光暈 </p> </td> 
   <td> <p> <span class="codeph">效果=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 內光暈 </p> </td> 
   <td> <p> <span class="codeph">效果=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-4c449fdf707b43858917fb271fa1fe96}

在圖層上增加三畫素寬、紅色不透明度為50%的邊框：

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

邊框會跟隨影像的Alpha色版或遮色片的輪廓。 設定`effect=1`會將框線置於內部邊緣。

使用預設效果設定（顏色除外），在影像中加入藍色投影：

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=`會在影像的右下邊緣加上一些邊界，以防止投影裁剪至影像邊界。

## 另請參閱 {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135)， [命令巨集%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
