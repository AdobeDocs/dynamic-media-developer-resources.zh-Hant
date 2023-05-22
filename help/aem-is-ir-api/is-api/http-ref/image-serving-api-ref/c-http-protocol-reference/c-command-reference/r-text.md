---
description: 圖層文本。 指定文本圖層的文本和格式內容。
solution: Experience Manager
title: 文字
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 5%

---

# 文字{#text}

圖層文本。 指定文本圖層的文本和格式內容。

` text= *`字串`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 字串 </span> </p> </td> 
  <td class="stentry"> <p>RTF字串或純文字檔案字串。 </p> </td> 
 </tr> 
</table>

所有字型、字型顏色和段落格式控制都使用RTF命令實現。 請參閱 [文本格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) 的雙曲餘切值。

`text=` 支援自動縮放文本以填充指定的圖層矩形 `size=`。

請參閱 [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)。

`text=` 支援自動調整文本圖層的大小以適合渲染的文本(當 `size=` 未指定或僅指定寬度時)。 請注意，在這種情況下，只有一個RTF對齊命令 `\ql`。 `\qr`, `\qc` 可以適用；否則返回錯誤。

## 屬性 {#section-8c0f020094a44c6b858454ef91ab4edf}

層屬性。 應用於 `layer=0` 如果 `layer=comp`。 與 `src=` 和 `textPs=` 同一層；上次 `text=`。 `textPs=`, `src=` 並確定這是影像還是文本圖層。 被效果層忽略。

## 預設 {#section-58958671e0ad479e8d5f6c1d41d7dc74}

無。

## 範例 {#section-d011f765ec5c418d814a821019b0eef0}

請參閱中的示例 [文本格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) 和 [示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 在 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另請參閱 {#section-207b779ab67342a5acd343e6bcc749c4}

[文本格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)。 [文本定位](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87)。 [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)。 [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)。 [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
