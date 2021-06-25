---
description: 圖層文字(與Adobe Photoshop相容)。 指定文本層的文本主體。
solution: Experience Manager
title: textPs
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 95f343ce-bea3-425e-9a25-d1d141a976d9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 4%

---

# textPs{#textps}

圖層文字(與Adobe Photoshop相容)。 指定文本層的文本主體。

`textPs= *`字串`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 字串</span> </span> </p> </td> 
  <td class="stentry"> <p>RTF字串。 </p></td> 
 </tr> 
</table>

所有字型、字型顏色和段落格式控制都使用RTF命令實現。

請參閱[文字格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)。

`textPs=` 支援擴展功能，如對齊、將文本流入由和/或定義的非矩 `textFlowPath=` 形區域， `textFlowXPath=`以及沿由定義的任意路徑呈現文 `textPath=`本。

## 屬性 {#section-a289dc26b6534b41998b1e241d5f2f92}

層屬性。 如果`layer=comp`，則套用至`layer=0`。 在同一層與`src=`和`text=`互斥。 `text=`、`textPs=`和`src=`的最後一個出現次數優先，並判斷這是影像還是文字層。 被效果層忽略。

## 預設 {#section-11c2ae2c96d64a0a9c207252df663e4d}

無。

## 另請參閱 {#section-5c2b25767d2b47b5be817271ab12e13c}

[文字格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textFlowXPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542),  [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd),  [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
