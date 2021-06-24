---
description: 圖層文字。 指定文本層的文本和格式化內容。
solution: Experience Manager
title: 文字
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 5%

---

# 文字{#text}

圖層文字。 指定文本層的文本和格式化內容。

` text= *`字串`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 字串 </span> </p> </td> 
  <td class="stentry"> <p>RTF字串或純文字字串。 </p> </td> 
 </tr> 
</table>

所有字型、字型顏色和段落格式控制都使用RTF命令實現。 如需詳細資訊，請參閱[文字格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) 。

`text=` 支援自動縮放文本以填充指定的圖層矩形 `size=`。

請參閱[textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)。

`text=` 支援自動調整文字層大小以符合呈現的文字( `size=` 未指定時或僅指定寬度時)。請注意，在這種情況下，只能應用RTF對齊命令`\ql`、`\qr`和`\qc`中的一個；否則會傳回錯誤。

## 屬性 {#section-8c0f020094a44c6b858454ef91ab4edf}

層屬性。 如果`layer=comp`，則套用至`layer=0`。 與`src=`和`textPs=`在同一層中互斥；「`text=`」、「`textPs=`」和「`src=`」的最後一個出現次數優先，並判斷這是影像還是文字層。 被效果層忽略。

## 預設 {#section-58958671e0ad479e8d5f6c1d41d7dc74}

無。

## 範例 {#section-d011f765ec5c418d814a821019b0eef0}

請參閱[文字格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)和[[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的範例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)。

## 另請參閱 {#section-207b779ab67342a5acd343e6bcc749c4}

[文本格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [文本定位](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
