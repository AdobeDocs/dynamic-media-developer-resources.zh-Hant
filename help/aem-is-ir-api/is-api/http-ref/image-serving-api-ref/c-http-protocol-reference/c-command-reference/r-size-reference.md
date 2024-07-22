---
title: 大小
description: 圖層大小。 指定圖層的大小或最大圖層大小，然後將rotate=、perspective=和extend=套用至圖層。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---

# 大小{#size}

圖層大小。 指定圖層的大小或最大圖層大小，然後將rotate=、perspective=和extend=套用至圖層。

` size= *`寬度`*, *`高度`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">寬度</span>，<span class="varname">高度</span> </span> </p> </td> 
  <td class="stentry"> <p>圖層大小限制，以畫素為單位（int、int、0或更大）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">寬度N </span>，<span class="varname">高度N </span> </span> </p> </td> 
  <td class="stentry"> <p>相對於圖層0大小標準化圖層大小限制（真實、真實、0.0...1.0）。 </p> </td> 
 </tr> 
</table>

指定影像圖層時， size=會限制圖層影像的寬度或/及高度。 影像已縮放為不大於`size=`。 如果指定了標準化大小，則它是相對於圖層0的大小。 如果同時指定&#x200B;*`width`*&#x200B;和&#x200B;*`height`*，來源影像會縮放（套用`crop=`之後），因此兩個維度都不會超過指定的大小。 在所有情況下，來源矩形的外觀比例都會保持不變。 *`width`*&#x200B;或&#x200B;*`height`*&#x200B;可以設為0；在此情況下，伺服器會根據影像的外觀比例計算值。

指定文字圖層時，`size=`會指定文字方塊大小。 *`width`*&#x200B;為必填；*`height`*&#x200B;可設為0，在此情況下，會使用佈局文字的高度做為圖層高度。 依預設，文字版面引擎會插入分行符號，以確保文字永遠水準符合可用的空間。 若指定&#x200B;*`height`*，不符合可用空間的行會被剪裁( `text=`)或省略( `textPs=`)。 `text=`支援其他調整模式；如需詳細資料，請參閱`textAttr=`。

指定純色圖層時，`size=`會定義確切的圖層大小；必須同時指定這兩個值（除非提供遮色片）。 如果同時指定`mask=`，則會調整遮色片影像大小以符合`size=`，就像在影像圖層中調整影像大小一樣。

## 屬性 {#section-5f254b66fcba49bcb63f9c9ea40b230c}

圖層屬性。 套用至圖層0 （若`layer=comp`）。 `layer=0`或`layer=comp`不允許`sizeN=`。 `sizeN=`僅允許在定義浮水印影像的目錄記錄中用於`layer=0`和`layer=comp`。 在這種情況下，`sizeN`會定義相對於要套用浮水印之複合影像的浮水印影像縮放。 若指定`size=`，則會忽略此圖層的`res=`和`scale=`。 被效果圖層忽略。

## 預設 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`，圖層大小未受限制。 針對影像圖層，套用任何`crop=`、`scale=`或`res=`作業後，就會根據圖層影像大小來決定圖層大小。 對於文字圖層，如果未指定`size=`，則會自動調整圖層大小以符合演算後的文字。

純色圖層需要完全指定的`size=`、`mask=`或`clipPath=`。

## 範例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

檢視[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的[範例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)。

## 另請參閱 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ， [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55)， [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)， [遮色片=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)， [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)， [文字圖層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
