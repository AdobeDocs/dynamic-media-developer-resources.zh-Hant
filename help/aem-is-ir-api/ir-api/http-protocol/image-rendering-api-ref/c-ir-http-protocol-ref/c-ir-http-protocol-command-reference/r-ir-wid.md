---
description: 回覆影像寬度。 指定演算後影像的縮放比例，讓回覆影像不會高於指定值，同時維持影像的外觀比例。
solution: Experience Manager
title: wid
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---


# wid{#wid}

回覆影像寬度。 指定演算後影像的縮放比例，讓回覆影像不會高於指定值，同時維持影像的外觀比例。

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>影像寬度（以像素為單位）（整數大於0）。 </p></td> 
 </tr> 
</table>

如果同時指定`wid=`和`hei=`且`wid`/ `hei`與影像的長寬比不同，則不填充影像。

`wid=` 並 `hei=` 共同定義伺服器傳回的影像大小。如果`scl=`在URL中位於`wid=`或`hei=`之後，則會取消這些命令，而`scl=`會定義伺服器傳回的影像大小。

但是，如果`wid=`或`hei=`在URL中位於`scl=`之後，它們會取消`scl=`和`wid=`/ `hei=`定義伺服器傳回的影像大小。

>[!NOTE]
>
>如果計算或預設回覆影像大小大於`attribute::MaxPix`，則會傳回錯誤。

## 屬性 {#section-2d067c6d371748e19cb157684700a49d}

可能發生在請求內的任何位置。 使用`wid=`、`hei=`或`scl=`調整影像大小並不會變更回應影像中內嵌的列印解析度值。 如果`scl=`發生在命令序列中`wid=`或`hei=`之後，則忽略。

## 預設 {#section-c7c6efa03d864592a3398b6f1de5a0b0}

如果未指定`wid=`、`hei=`和`scl=`，則回復影像將縮放為適合`attribute::DefaultPix`定義的大小。 如果`attribute::DefaultPix`為空白，則回覆影像的大小將與暈映的檢視影像相同。

## 另請參閱 {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29) [,attributesMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
