---
title: scl
description: 縮放視圖。 相對於全解析度視頻，按指定的縮放因子縮放渲染的影像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 2%

---

# scl{#scl}

縮放視圖。 相對於全解析度視頻，按指定的縮放因子縮放渲染的影像。

`scl= *`inv系數`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> inv系數</span> </span> </p></td> 
  <td class="stentry"> <p>反比例因子（實數、1.0或更大）。 </p></td> 
 </tr> 
</table>

如果 `scl=` 後 `wid=` 或 `hei=` 命令，並 `scl=` 定義伺服器返回的映像的大小。

但是，如果 `wid=` 或 `hei=` 後 `scl=` 的子菜單。 `scl=` 和 `wid=`/ `hei=` 定義伺服器返回的映像大小。

>[!NOTE]
>
>如果計算的或預設的答復影像大小大於 `attribute::MaxPix`。

## 屬性 {#section-170458cbd6984bd59a3434431258b20f}

請求中的任何位置都可能發生。 如果忽略 `wid=` 或 `hei=` 在 `scl=` 的子菜單。

調整影像大小 `scl=` 不更改嵌入在響應影像中的打印解析度值。

## 預設 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

如果 `wid=`。 `hei=`或 `scl=` 未指定，將縮放回復影像以適合由定義的大小 `attribute::DefaultPix`。 如果 `attribute::DefaultPix` 為空，回復影像的大小與視頻的視圖影像大小相同。

## 另請參閱 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) 。 [黑=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)。 [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)。 [屬性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)。 [屬性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
