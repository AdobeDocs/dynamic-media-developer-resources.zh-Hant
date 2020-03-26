---
description: 回覆影像高度。 指定演算後影像的縮放比例，使回覆影像的高度不大於指定值，同時維持影像的長寬比。
seo-description: 回覆影像高度。 指定演算後影像的縮放比例，使回覆影像的高度不大於指定值，同時維持影像的長寬比。
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

回覆影像高度。 指定演算後影像的縮放比例，使回覆影像的高度不大於指定值，同時維持影像的長寬比。

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>回覆影像高度（以像素為單位，整數大於0）。 </p></td> 
 </tr> 
</table>

如果同時指定和指定 `wid=` 且寬 `hei=` 度／高度不同於影像的長寬比，則不填充影像。

`wid=` 並 `hei=` 共同定義伺服器傳回的影像大小。 如 `scl=` 果出現在 `wid=` URL後或 `hei=` URL中，則會取消這些命令，並 `scl=` 定義伺服器傳回的影像大小。

但是，如 `wid=` 果或 `hei=` 在URL中 `scl=` 出現，則會取消和 `scl=` / `wid=``hei=` 定義伺服器傳回的影像大小。

>[!NOTE]
>
>如果計算或預設的回覆影像大小大於，則會傳回錯誤 `attribute::MaxPix`。

## 屬性 {#section-6cbc6acd37c847beab84c896ac25280c}

可能發生在請求內的任何位置。 使用、 `wid=`或 `hei=``scl=` 不會變更回應影像中內嵌的列印解析度值。 如果在命 `scl=` 令序列中 `wid=` 和/ `hei=` 或之後發生，則忽略。

## 預設 {#section-61043f6c1f5d450883ff9e5eafd95955}

如果未 `wid=`指 `hei=`定、 `scl=` 也未指定，則會縮放回覆影像，使其符合所定義的大小 `attribute::DefaultPix`。 如 `attribute::DefaultPix` 果空白，則回覆影像的大小與暈映的檢視影像相同。

## 另請參閱 {#section-7ba51379f1e2421c92d3592d20a37734}

[屬性：:Pix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ，屬性：:MaxPix [,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)wid= [,](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)scl= [](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)[, resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
