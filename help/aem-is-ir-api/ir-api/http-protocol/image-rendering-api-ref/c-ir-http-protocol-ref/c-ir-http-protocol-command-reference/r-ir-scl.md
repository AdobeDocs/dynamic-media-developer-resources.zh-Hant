---
description: 縮放檢視。 相對於全解析度暈映，依指定的縮放比例來縮放轉換的影像。
solution: Experience Manager
title: scl
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 3%

---


# scl{#scl}

縮放檢視。 相對於全解析度暈映，依指定的縮放比例來縮放轉換的影像。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>反比例系數（實數、1.0或更高）。 </p></td> 
 </tr> 
</table>

如果`scl=`在URL中位於`wid=`或`hei=`之後，則會取消這些命令，而`scl=`會定義伺服器傳回的影像大小。

但是，如果`wid=`或`hei=`在URL中位於`scl=`之後，它們會取消`scl=`和`wid=`/ `hei=`定義伺服器傳回的影像大小。

>[!NOTE]
>
>如果計算或預設回覆影像大小大於`attribute::MaxPix`，則會傳回錯誤。

## 屬性 {#section-170458cbd6984bd59a3434431258b20f}

可能發生在請求內的任何位置。 如果`wid=`或`hei=`發生在命令序列中`scl=`之後，則忽略。

使用`scl=`調整影像大小並不會變更回應影像中內嵌的列印解析度值。

## 預設 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

如果未指定`wid=`、`hei=`或`scl=`，則回復影像將縮放為適合`attribute::DefaultPix`定義的大小。 如果`attribute::DefaultPix`為空白，則回覆影像的大小與暈映的檢視影像相同。

## 另請參閱 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)，屬 [性：MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657) [,MaxPix屬性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
