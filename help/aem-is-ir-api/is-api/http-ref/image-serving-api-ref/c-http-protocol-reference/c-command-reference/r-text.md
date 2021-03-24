---
description: 圖層文字。 指定文字圖層的文字和格式內容。
solution: Experience Manager
title: 文字
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 5%

---


# 文字{#text}

圖層文字。 指定文字圖層的文字和格式內容。

` text= *`字串`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 字串 </span> </p> </td> 
  <td class="stentry"> <p>RTF字串或純文字字串。 </p> </td> 
 </tr> 
</table>

所有字型、字型色彩和段落格式控制都是使用RTF命令實現的。 如需詳細資訊，請參閱[文字格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)。

`text=` 支援自動縮放文字，以填滿指定的圖層矩形 `size=`。

請參閱[textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)。

`text=` 支援文字圖層自動調整大小，以符合轉譯的文字( `size=` 未指定時或僅指定寬度時)。請注意，在這種情況下，只能應用RTF對齊命令`\ql`、`\qr`和`\qc`中的一個；否則會傳回錯誤。

## 屬性 {#section-8c0f020094a44c6b858454ef91ab4edf}

層屬性。 如果`layer=comp`，則套用至`layer=0`。 與`src=`和`textPs=`在同一層中互斥；上次出現`text=`、`textPs=`和`src=`的情況會普遍出現，並判斷這是影像還是文字圖層。 被效果圖層忽略。

## 預設 {#section-58958671e0ad479e8d5f6c1d41d7dc74}

無。

## 範例 {#section-d011f765ec5c418d814a821019b0eef0}

請參閱[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中[文字格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)和[範例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)中的範例。

## 另請參閱 {#section-207b779ab67342a5acd343e6bcc749c4}

[文字格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)化文字定位 [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87)src= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)Attr= [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d) [，文字Ps=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
