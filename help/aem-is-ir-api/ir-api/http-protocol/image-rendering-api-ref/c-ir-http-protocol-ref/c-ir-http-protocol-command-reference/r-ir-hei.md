---
description: 回覆影像高度。 指定呈現影像的縮放比例，使得回覆影像的高度不大於指定值，同時維持影像的長寬比。
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---

# 平{#hei}

回覆影像高度。 指定呈現影像的縮放比例，使得回覆影像的高度不大於指定值，同時維持影像的長寬比。

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>以像素表示回覆影像高度（大於0的整數）。 </p></td> 
 </tr> 
</table>

如果同時指定`wid=`和`hei=`且寬度/高度與影像的長寬比不同，則不會補充影像。

`wid=` 和 `hei=` 一起定義伺服器傳回之影像的大小。如果`scl=`在URL中位於`wid=`或`hei=`之後，它會取消這些命令，而`scl=`會定義伺服器傳回的影像大小。

不過，如果`wid=`或`hei=`在URL中位於`scl=`之後，則會取消`scl=`和`wid=`/ `hei=`定義伺服器傳回的影像大小。

>[!NOTE]
>
>如果計算或預設的回覆影像大小大於`attribute::MaxPix`，則會傳回錯誤。

## 屬性 {#section-6cbc6acd37c847beab84c896ac25280c}

可能發生在要求內的任何位置。 使用`wid=`、`hei=`或`scl=`調整影像大小不會更改響應影像中嵌入的打印解析度值。 如果`scl=`發生在命令序列的`wid=`之後，和/或`hei=`，則忽略。

## 預設 {#section-61043f6c1f5d450883ff9e5eafd95955}

如果未指定`wid=`、`hei=`或`scl=`，則回復影像會縮放以符合`attribute::DefaultPix`所定義的大小。 如果`attribute::DefaultPix`空白，則回覆影像的大小與暈映者的檢視影像大小相同。

## 另請參閱 {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
