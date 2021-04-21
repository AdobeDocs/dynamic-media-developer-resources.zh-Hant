---
description: 文字流動區域。 指定應將文字與textPs=所指定的一或多個區域整合。
solution: Experience Manager
title: textFlowPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---


# textFlowPath{#textflowpath}

文字流動區域。 指定應將文字與textPs=所指定的一或多個區域整合。

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition  </span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p> </td> 
 </tr> 
</table>

如需詳細資訊，包括&#x200B;*`pathDefinition`*&#x200B;的說明，請參閱[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)。

當`textFlowPath=`存在時，將忽略RTF邊界命令`\margl`、`\margr`、`\margt`和`\margb`。 如果未指定路徑定義，則會忽略`textFlowPath=`。

## 屬性 {#section-b68dc887c6534ce8982cad740b3aeaa4}

文字圖層屬性（僅限`textPs=`）。 被其他圖層忽略。 如果為`layer=comp`指定，則套用至`layer=0`。

## 預設 {#section-68c4559b9e8242059b82e5a39a455dfc}

與圖層矩形相同；文字會填滿整個圖層矩形。

## 另請參閱 {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) clipPath= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)FlowPath= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)Angle= [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15) [, textLayers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
