---
description: 圖層大小。 指定圖層的大小或最大圖層大小，然後將rotate=、perspective=和extend=應用於圖層。
seo-description: 圖層大小。 指定圖層的大小或最大圖層大小，然後將rotate=、perspective=和extend=應用於圖層。
seo-title: 大小
solution: Experience Manager
title: 大小
topic: Scene7 Image Serving - Image Rendering API
uuid: c9c13062-7974-4dd9-aff4-f9502bcf442e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 大小{#size}

圖層大小。 指定圖層的大小或最大圖層大小，然後將rotate=、perspective=和extend=應用於圖層。

` size= *`寬`*, *`高`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 寬 </span>度 <span class="varname"> ，高 </span> 度 </span> </p> </td> 
  <td class="stentry"> <p>圖層大小約束（以像素為單位）（int、int、0或更大）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 寬 <span class="varname"> 度N </span>，高 <span class="varname"> 度N </span></span> </p> </td> 
  <td class="stentry"> <p>圖層大小約束相對於圖層0大小標準化（實數、實數、0.0...1.0）。 </p> </td> 
 </tr> 
</table>

為影像圖層指定時，size=會限製圖層影像的寬度、高度或兩者。 影像將會縮放至不大於 `size=`。 如果指定了標準化大小，則它相對於層0的大小。 如果同時 *`width`* 指定 *`height`* 和，則源影像將縮放（在應用後）, `crop=` 以便尺寸均不超過指定大小。 在所有情況下，源矩形的長寬比都保持不變。 或 *`width`* 者 *`height`* 可設為0;在這種情況下，值由伺服器根據影像的長寬比來計算。

為文本圖層指定時， `size=` 指定文本框大小。 *`width`* 為必要項目；可 *`height`* 以設定為0，在這種情況下，排版文本的高度用作圖層高度。 依預設，文字版面引擎會插入分行，以確保文字始終以水準方式放入可用空間。 如果 *`height`* 指定，不符合可用空間的線將被裁切( `text=`)或省略( `textPs=`)。 `text=` 支援額外的配合模式；有關詳細 `textAttr=` 資訊，請參閱。

當為純色層指定時，會定 `size=` 義精確的層大小；必須指定兩個值（除非提供遮色片）。 如果 `mask=` 也指定遮色片影像，則會調整遮色片影像的大小，以 `size=` 符合影像圖層中影像縮放的相同方式。

## 屬性 {#section-5f254b66fcba49bcb63f9c9ea40b230c}

層屬性。 如果適用，則套用至圖層0 `layer=comp`。 `sizeN=` 不允許 `layer=0` 或 `layer=comp`。 `sizeN=` 僅允許在定 `layer=0` 義水 `layer=comp` 印影像的目錄記錄中。 在這種情況下， `sizeN` 定義水印影像相對於要應用水印的合成影像的縮放比例。 如果 `size=` 已指定， `res=` 則 `scale=` 會忽略此層。 被效果圖層忽略。

## 預設 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`，則圖層大小不受約束。 然後，對於影像圖層，在應用了任何、或操作之後，根據圖 `crop=`層影像 `scale=`大 `res=` 小確定圖層大小。 對於文本圖層，如 `size=` 果未指定，圖層將自動調整大小，以符合渲染的文本。

純色圖層需要完全指 `size=`定、 `mask=`或 `clipPath=`。

## 範例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

請參 [閱範本中](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 的 [範例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另請參閱 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)[，剪輯路徑=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)[res=文本圖層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
