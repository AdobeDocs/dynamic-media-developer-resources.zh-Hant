---
description: 回覆影像高度。 指定演算後影像的縮放比例，使回覆影像的高度不大於指定值，同時維持影像的長寬比。
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 2%

---


# hei{#hei}

回覆影像高度。 指定演算後影像的縮放比例，使回覆影像的高度不大於指定值，同時維持影像的長寬比。

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>回覆影像高度（以像素為單位，整數大於0）。 </p></td> 
 </tr> 
</table>

如果同時指定`wid=`和`hei=`且寬度／高度不同於影像的長寬比，則不填充影像。

`wid=` 並 `hei=` 共同定義伺服器傳回的影像大小。如果`scl=`在URL中位於`wid=`或`hei=`之後，則會取消這些命令，而`scl=`會定義伺服器傳回的影像大小。

但是，如果`wid=`或`hei=`在URL中位於`scl=`之後，它們會取消`scl=`和`wid=`/ `hei=`定義伺服器傳回的影像大小。

>[!NOTE]
>
>如果計算或預設回覆影像大小大於`attribute::MaxPix`，則會傳回錯誤。

## 屬性 {#section-6cbc6acd37c847beab84c896ac25280c}

可能發生在請求內的任何位置。 使用`wid=`、`hei=`或`scl=`調整影像大小並不會變更回應影像中內嵌的列印解析度值。 如果`scl=`發生在命令序列中`wid=`和／或`hei=`之後，則忽略。

## 預設 {#section-61043f6c1f5d450883ff9e5eafd95955}

如果未指定`wid=`、`hei=`和`scl=`，則回復影像將縮放為適合`attribute::DefaultPix`定義的大小。 如果`attribute::DefaultPix`為空白，則回覆影像的大小與暈映的檢視影像相同。

## 另請參閱 {#section-7ba51379f1e2421c92d3592d20a37734}

[屬性：::Pix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ，屬 [性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), wid= [, ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)scl= [](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29) [,resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
