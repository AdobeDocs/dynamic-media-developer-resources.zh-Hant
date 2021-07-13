---
description: 縮放視圖。 根據指定的縮放因子，相對於全解析度暈映縮放渲染的影像。
solution: Experience Manager
title: scl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# scl{#scl}

縮放視圖。 根據指定的縮放因子，相對於全解析度暈映縮放渲染的影像。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>反比例因子（實數、1.0或更大）。 </p></td> 
 </tr> 
</table>

如果`scl=`在URL中位於`wid=`或`hei=`之後，它會取消這些命令，而`scl=`會定義伺服器傳回的影像大小。

不過，如果`wid=`或`hei=`在URL中位於`scl=`之後，則會取消`scl=`和`wid=`/ `hei=`定義伺服器傳回的影像大小。

>[!NOTE]
>
>如果計算或預設的回覆影像大小大於`attribute::MaxPix`，則會傳回錯誤。

## 屬性 {#section-170458cbd6984bd59a3434431258b20f}

可能發生在要求內的任何位置。 如果在命令序列中`wid=`或`hei=`出現在`scl=`之後，則忽略。

使用`scl=`調整影像大小不會更改響應影像中嵌入的打印解析度值。

## 預設 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

如果未指定`wid=`、`hei=`或`scl=`，則回復影像會縮放以符合`attribute::DefaultPix`所定義的大小。 如果`attribute::DefaultPix`空白，則回覆影像的大小與暈映者的檢視影像大小相同。

## 另請參閱 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3),  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
