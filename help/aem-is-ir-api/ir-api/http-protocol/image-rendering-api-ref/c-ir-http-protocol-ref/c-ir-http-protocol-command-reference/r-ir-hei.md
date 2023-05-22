---
title: hei
description: 回復影像高度。 指定渲染影像的縮放比例，以便回復影像的高度不大於指定值，同時保持影像的長寬比。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 2%

---

# hei{#hei}

回復影像高度。 指定渲染影像的縮放比例，以便回復影像的高度不大於指定值，同時保持影像的長寬比。

`hei= *`谷`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 谷</span> </span> </p></td> 
  <td class="stentry"> <p>答復影像高度（以像素為單位）（大於0的整數）。 </p></td> 
 </tr> 
</table>

如果兩者兼有，則不填充影像 `wid=` 和 `hei=` 寬度/高度與影像的長寬比不同。

`wid=` 和 `hei=` 共同定義伺服器返回的映像的大小。 如果 `scl=` 後 `wid=` 或 `hei=` 命令，並 `scl=` 定義伺服器返回的映像的大小。

但是，如果 `wid=` 或 `hei=` 後 `scl=` 的子菜單。 `scl=` 和 `wid=`/ `hei=` 定義伺服器返回的映像大小。

>[!NOTE]
>
>如果計算的或預設的答復影像大小大於 `attribute::MaxPix`。

## 屬性 {#section-6cbc6acd37c847beab84c896ac25280c}

請求中的任何位置都可能發生。 調整影像大小 `wid=`。 `hei=`或 `scl=` 不更改嵌入在響應影像中的打印解析度值。 如果忽略 `scl=` 在 `wid=` 和/或 `hei=` 的子菜單。

## 預設 {#section-61043f6c1f5d450883ff9e5eafd95955}

如果 `wid=`。 `hei=`或 `scl=` 未指定，將縮放回復影像以適合由定義的大小 `attribute::DefaultPix`。 如果 `attribute::DefaultPix` 為空，回復影像的大小與視頻的視圖影像大小相同。

## 另請參閱 {#section-7ba51379f1e2421c92d3592d20a37734}

[屬性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) 。 [屬性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)。 [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)。 [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)。 [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
