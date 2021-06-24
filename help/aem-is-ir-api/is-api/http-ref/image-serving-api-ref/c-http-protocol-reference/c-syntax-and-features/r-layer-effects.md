---
description: Photoshop樣式的層陰影和輝光效果是使用特殊的子層（效果層）實現的，這些子層可附加到任何層（父層），包括layer=0和layer=comp。
solution: Experience Manager
title: 圖層效果
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 2%

---

# 圖層效果{#layer-effects}

Photoshop樣式的層陰影和輝光效果是使用特殊的子層（效果層）實現的，這些子層可附加到任何層（父層），包括layer=0和layer=comp。

儘管效果層支援許多標準影像和圖層屬性和命令，但它們不是作為通用圖層，也不支援獨立的影像或文本資料。

任何數量的圖層效果都可以附加到單個父層。

## 內外效應 {#section-2dade7ee98e041d1b4d1725e6f98a515}

*內部* 效果會呈現在父層的頂部，並且僅在父層的不透明區域中可見。*外部* 效果在父層後呈現（因此它們永遠不會在父層的不透明區域內可見），並且可以位於複合畫布內的任意位置。通過使用`effect=`命令指定正或負效應層號來選擇內或外效應。 `effect=`命令還控制連接到同一父層的多個效果層之間的z順序。

## 與上層的關係 {#section-eb8bfc4f754a42fc973b562821d6f2d3}

效果層會自動調整大小並定位以與父層一致（即，效果層繼承父層的`size=`和`origin=`值）。 `pos=` 可用於將效果圖層從父層移開，這通常是放置和內陰影效果所需的。對於標準層`pos=`，指定此層的原點與層0之間的偏移，而對於效果層`pos=`，指定效果層的原點與父層之間的偏移。

## 支援的命令和屬性 {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

效果層接受以下命令和屬性：

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

效果圖層中包含的所有其他影像和圖層命令都將被忽略。

## 預設效果宏 {#section-a01e8dcc87c94495b54a6dfb21d2a718}

為方便使用圖層效果，IS提供了兩個宏，其中包含預設影像目錄`$shadow$`和`$glow$`，它們為效果圖層屬性提供與Photoshop圖層效果類似的預設值。 下表列出了應使用哪些效果命令和宏來實施預設層效果。 自然地，在宏中指定的任何屬性都可以在URL中修改，或者可以建立替代的宏來實施自定義圖層效果。

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 所需效果</b> </th> 
   <th class="entry"> <b> 命令</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> 陰影 </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 內陰影 </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 外光暈 </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 內光暈 </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-4c449fdf707b43858917fb271fa1fe96}

在圖層中加上3個像素寬、紅色的邊框，其不透明度為50%:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

邊框將跟隨影像的Alpha通道或蒙版的輪廓。 設定`effect=1`會將邊框改為放在內邊緣。

使用預設效果設定（顏色除外）將藍色陰影添加到影像中：

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` 在影像的右下邊添加一點邊距，這樣可防止陰影被剪切到影像邊界。

## 另請參閱 {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [命令宏%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
