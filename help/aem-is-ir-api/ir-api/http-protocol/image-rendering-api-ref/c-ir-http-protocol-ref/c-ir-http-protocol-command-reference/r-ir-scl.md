---
description: 縮放檢視。 相對於全解析度暈映，依指定的縮放比例來縮放轉換的影像。
seo-description: 縮放檢視。 相對於全解析度暈映，依指定的縮放比例來縮放轉換的影像。
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 04839c44-01b6-4fa2-9eda-bbb0f2822db4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

縮放檢視。 相對於全解析度暈映，依指定的縮放比例來縮放轉換的影像。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span></span> </p></td> 
  <td class="stentry"> <p>反比例系數（實數、1.0或更高）。 </p></td> 
 </tr> 
</table>

如 `scl=` 果出現在 `wid=` URL後或 `hei=` URL中，則會取消這些命令，並 `scl=` 定義伺服器傳回的影像大小。

但是，如 `wid=` 果或 `hei=` 在URL中 `scl=` 出現，則會取消和 `scl=` / `wid=``hei=` 定義伺服器傳回的影像大小。

>[!NOTE]
>
>如果計算或預設的回覆影像大小大於，則會傳回錯誤 `attribute::MaxPix`。

## 屬性 {#section-170458cbd6984bd59a3434431258b20f}

可能發生在請求內的任何位置。 在命令序 `wid=` 列中 `hei=` 出現 `scl=` 或發生後忽略。

使用調整影像大小 `scl=` 並不會變更回應影像中內嵌的列印解析度值。

## 預設 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

如果未指 `wid=`定， `hei=` 也未 `scl=` 指定，則會縮放回覆影像以符合由定義的大小 `attribute::DefaultPix`。 如 `attribute::DefaultPix` 果空白，則回覆影像的大小與暈映的檢視影像相同。

## 另請參閱 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)，屬 [性：MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)[,MaxPix屬性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
