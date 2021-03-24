---
description: 圖層文字(與Adobe Photoshop相容)。 指定文本圖層的文本主體。
solution: Experience Manager
title: textPs
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 4%

---


# textPs{#textps}

圖層文字(與Adobe Photoshop相容)。 指定文本圖層的文本主體。

`textPs= *`字串`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 字串</span> </span> </p> </td> 
  <td class="stentry"> <p>RTF字串。 </p></td> 
 </tr> 
</table>

所有字型、字型色彩和段落格式控制都是使用RTF命令實現的。

請參閱[文字格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)。

`textPs=` 支援擴充功能，例如對齊、將文字流入以及 `textFlowPath=` /或定義的非矩形區域 `textFlowXPath=`，以及沿著以定義的任意路徑演算文字 `textPath=`。

## 屬性 {#section-a289dc26b6534b41998b1e241d5f2f92}

層屬性。 如果`layer=comp`，則套用至`layer=0`。 在同一層中與`src=`和`text=`互斥。 上次出現`text=`、`textPs=`和`src=`時，會優先顯示，並判斷這是影像還是文字圖層。 被效果圖層忽略。

## 預設 {#section-11c2ae2c96d64a0a9c207252df663e4d}

無。

## 另請參閱 {#section-5c2b25767d2b47b5be817271ab12e13c}

[文本格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [src=text](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textText=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)FlowAttr [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) [,FlowTextFlowXPTEXT=TextFormatting=,TextText=Path=ThathAthAth=AthTh=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
