---
description: Photoshop風格的圖層陰影和發光效果是使用特殊的子圖層（效果圖層）來實現的，子圖層可附加到任何圖層（父圖層），包括layer=0和layer=comp。
solution: Experience Manager
title: 圖層效果
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 2%

---


# 圖層效果{#layer-effects}

Photoshop風格的圖層陰影和發光效果是使用特殊的子圖層（效果圖層）來實現的，子圖層可附加到任何圖層（父圖層），包括layer=0和layer=comp。

雖然效果圖層支援許多標準影像和圖層屬性和命令，但它們並非一般用途的圖層，也不支援獨立的影像或文字資料。

任何數量的圖層效果都可附加至單一父層。

## 內外效果{#section-2dade7ee98e041d1b4d1725e6f98a515}

*內部* 效果會在父層的頂部呈現，並且僅在父層的不透明區域中可見。*外部* 效果會在父圖層後面呈現（因此它們永遠不會出現在父圖層的不透明區域中），而且可以放置在複合畫布內的任何位置。通過使用`effect=`命令指定正或負效果層號來選擇內或外效果。 `effect=`命令還控制連接到同一父層的多個效果圖層之間的z順序。

## 與父層{#section-eb8bfc4f754a42fc973b562821d6f2d3}的關係

特效圖層會自動調整大小並定位以與父層一致（即特效圖層繼承父層的`size=`和`origin=`值）。 `pos=` 可用來將效果圖層從父圖層移開，這通常是下垂和內陰影效果的必要項。對於標準層`pos=`，指定此層的起點和層0之間的偏移，對於效果層`pos=`，指定效果層的起點和父層之間的偏移。

## 支援的命令和屬性{#section-035fc6bcba7d4e7ab4bd46687c1d8879}

效果圖層接受下列命令和屬性：

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

## 預設效果宏{#section-a01e8dcc87c94495b54a6dfb21d2a718}

為方便使用圖層效果，IS提供兩個具有預設影像目錄（`$shadow$`和`$glow$`）的巨集，這些目錄為效果圖層屬性(類似於Photoshop圖層效果)提供預設值。 下表列出了應使用哪些效果命令和宏來實現預設層效果。 自然地，宏中指定的任何屬性都可以在URL中修改，或者建立替代宏以實施自定義圖層效果。

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

在圖層中加入3個像素寬的紅色邊框，其不透明度為50%:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

邊框會遵循影像的Alpha色版或遮色片的輪廓。 設定`effect=1`會將邊框改為置於內側邊緣。

使用預設效果設定（顏色除外），將藍色的下垂式陰影新增至影像：

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` 在影像的右下方加上一小段邊界，以避免陰影被裁切至影像邊界。

## 另請參閱 {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135)，命 [令宏%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
