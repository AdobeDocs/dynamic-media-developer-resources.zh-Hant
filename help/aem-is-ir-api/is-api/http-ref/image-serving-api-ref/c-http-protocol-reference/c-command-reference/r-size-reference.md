---
description: 圖層大小。 指定圖層的大小或最大圖層大小，然後將rotate=、perspective=和extend=應用於圖層。
solution: Experience Manager
title: 大小
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 1%

---


# 大小{#size}

圖層大小。 指定圖層的大小或最大圖層大小，然後將rotate=、perspective=和extend=應用於圖層。

` size= *`寬`*, *`高`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 寬度 </span>，高 <span class="varname"> 度  </span> </span> </p> </td> 
  <td class="stentry"> <p>圖層大小約束（以像素為單位）（int、int、0或更大）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN  </span>,  <span class="varname"> heightN  </span> </span> </p> </td> 
  <td class="stentry"> <p>圖層大小約束相對於圖層0大小標準化（實數、實數、0.0...1.0）。 </p> </td> 
 </tr> 
</table>

為影像圖層指定時，size=會限製圖層影像的寬度、高度或兩者。 影像將會縮放至不大於`size=`。 如果指定了標準化大小，則它相對於層0的大小。 如果同時指定&#x200B;*`width`*&#x200B;和&#x200B;*`height`*，則源影像將縮放（在應用`crop=`後），以使任何尺寸均不超過指定的大小。 在所有情況下，源矩形的長寬比都保持不變。 *`width`*&#x200B;或&#x200B;*`height`*&#x200B;可設為0;在這種情況下，值由伺服器根據影像的長寬比來計算。

為文本層指定時，`size=`指定文本框大小。 *`width`* 為必要項目； *`height`* 可設為0，在此情況下，排版文字的高度會用作圖層高度。依預設，文字版面引擎會插入分行，以確保文字始終以水準方式放入可用空間。 如果指定&#x200B;*`height`*，則不符合可用空間的行將被裁切(`text=`)或省略(`textPs=`)。 `text=` 支援額外的配合模式；有關詳細 `textAttr=` 資訊，請參閱。

當為純色層指定時，`size=`會定義精確的層大小；必須指定兩個值（除非提供遮色片）。 如果還指定了`mask=`，則蒙版影像的大小將與在影像圖層中縮放影像的方式相同，以適合`size=`。

## 屬性 {#section-5f254b66fcba49bcb63f9c9ea40b230c}

層屬性。 如果`layer=comp`，則套用至層0。 `sizeN=` 不允許 `layer=0` 或 `layer=comp`。`sizeN=` 僅允許在定 `layer=0` 義水 `layer=comp` 印影像的目錄記錄中使用。在這種情況下，`sizeN`定義水印影像相對於要應用水印的複合影像的縮放比例。 如果指定`size=`，則會忽略此層的`res=`和`scale=`。 被效果圖層忽略。

## 預設 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`，則圖層大小不受約束。對於影像層，然後根據應用了任何`crop=`、`scale=`或`res=`操作後的圖層影像大小確定圖層大小。 對於文本圖層，如果未指定`size=`，則圖層將自動調整大小，以符合渲染的文本。

單色圖層需要完全指定的`size=`、`mask=`或`clipPath=`。

## 範例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

請參閱[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的[範例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)。

## 另請參閱 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ,  [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55),  [textAttr=mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)，剪 [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) [輯路徑=res=文本圖層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
