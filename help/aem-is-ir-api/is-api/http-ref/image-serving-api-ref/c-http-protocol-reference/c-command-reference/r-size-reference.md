---
description: 層大小。 在將rotate=、perspective=和extend=應用於圖層之前，指定圖層的大小或最大圖層大小。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# 大小{#size}

層大小。 在將rotate=、perspective=和extend=應用於圖層之前，指定圖層的大小或最大圖層大小。

` size= *`寬度`*, *`高度`*`

` sizeN= *`寬度N`*, *`高度N`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 寬度 </span>。 <span class="varname"> 高度 </span> </span> </p> </td> 
  <td class="stentry"> <p>圖層大小約束（以像素為單位）（int、int、0或更大）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 寬度N </span>。 <span class="varname"> 高度N </span> </span> </p> </td> 
  <td class="stentry"> <p>層大小約束相對於層0大小進行歸一化（實數、實數、0.0...1.0）。 </p> </td> 
 </tr> 
</table>

為影像圖層指定時， size=會限製圖層影像的寬度或高度，或同時限制兩者。 將影像縮放為不大於 `size=`。 如果指定了歸一化大小，則它與層0的大小相關。 如果兩者都 *`width`* 和 *`height`* 指定，將縮放源影像(在 `crop=` 應用)，以使兩個尺寸均不超過指定大小。 在所有情況下都保持源矩形的長寬比。 要麼 *`width`* 或 *`height`* 可設定為0;在這種情況下，該值由伺服器基於影像的長寬比計算。

為文本層指定時， `size=` 指定文本框大小。 *`width`* 需要； *`height`* 可以設定為0，在這種情況下，將佈局文本的高度用作圖層高度。 預設情況下，文本佈局引擎會插入換行符，以確保文本始終水準放入可用空間。 如果 *`height`* 指定，不適合可用空間的線將被修剪( `text=`)或省略( `textPs=`)。 `text=` 支援附加的配套模式；參考 `textAttr=` 的雙曲餘切值。

為實色層指定時， `size=` 定義確切的層大小；必須指定這兩個值（除非提供掩碼）。 如果 `mask=` 還指定了，蒙版影像的大小與 `size=` 在影像層中縮放影像的方式相同。

## 屬性 {#section-5f254b66fcba49bcb63f9c9ea40b230c}

層屬性。 如果為 `layer=comp`。 `sizeN=` 不允許 `layer=0` 或 `layer=comp`。 `sizeN=` 允許 `layer=0` 和 `layer=comp` 僅在定義水印影像的目錄記錄中。 在這個例子中， `sizeN` 定義水印影像相對於要應用水印的複合影像的縮放比例。 如果 `size=` 已指定， `res=` 和 `scale=` 將忽略此層。 被效果層忽略。

## 預設 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`，圖層大小不受約束。 對於影像層，然後根據任何之後的圖層影像大小確定圖層大小 `crop=`。 `scale=`或 `res=` 操作已應用。 對於文本圖層，如果 `size=` 未指定，圖層的大小將自動調整為適合渲染的文本。

實色層要求完全指定 `size=`的 `mask=`或 `clipPath=`。

## 範例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

請參閱 [示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 在 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另請參閱 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[比例=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) 。 [雷斯=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55)。 [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)。 [掩碼=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)。 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)。 [文本圖層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
