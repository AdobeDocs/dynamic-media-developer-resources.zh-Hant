---
title: scl
description: 縮放檢視。 依照指定的縮放係數縮放演算後的影像（相對於完整解析度暈映）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---

# scl{#scl}

縮放檢視。 依照指定的縮放係數縮放演算後的影像（相對於完整解析度暈映）。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>反比例因子（實數、1.0或更高）。 </p></td> 
 </tr> 
</table>

如果`scl=`在URL中的`wid=`或`hei=`之後，它會取消這些命令，並且`scl=`會定義伺服器傳回的影像大小。

不過，如果URL中的`wid=`或`hei=`在`scl=`之後，它們會取消`scl=`且`wid=`/`hei=`會定義伺服器傳回的影像大小。

>[!NOTE]
>
>如果計算的或預設的回覆影像大小大於`attribute::MaxPix`，則會傳回錯誤。

## 屬性 {#section-170458cbd6984bd59a3434431258b20f}

可能發生在請求中的任何位置。 如果命令序列中的`wid=`之後發生`hei=`或`scl=`，則忽略此專案。

使用`scl=`調整影像大小不會變更內嵌在回應影像中的列印解析度值。

## 預設 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

如果未指定`wid=`、`hei=`或`scl=`，則回覆影像會調整為符合`attribute::DefaultPix`所定義的大小。 如果`attribute::DefaultPix`是空的，則回覆影像的大小將與暈映的檢視影像相同。

## 另請參閱 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ， [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)， [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)， [attribute：：MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)， [attribute：：DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
