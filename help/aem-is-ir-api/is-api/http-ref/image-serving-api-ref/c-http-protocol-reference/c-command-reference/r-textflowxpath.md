---
description: 文字排除區域。 指定要從文字流中排除的一或多個區域。
seo-description: 文字排除區域。 指定要從文字流中排除的一或多個區域。
seo-title: textFlowXPath
solution: Experience Manager
title: textFlowXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: ce833ae7-e774-4954-a521-b6247e75f6eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# textFlowXPath{#textflowxpath}

文字排除區域。 指定要從文字流中排除的一或多個區域。

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
</table>

如需 [其他資訊](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) ，包括的說明，請參閱clipPath= *`pathDefinition`*。 如果未指定路徑定義，則 `textFlowXPath=` 會忽略。

## 屬性 {#section-cd1ebb151d4a405fbfc508d46522d686}

文字圖層屬性( `textPs=` 僅限)。 被其他圖層忽略，或在未指定時 `textFlowPath=`。 如果已 `layer=0` 指定，則套用至 `layer=comp`。

## 預設 {#section-9405cda904684d829ed12a9e40a4dc46}

無。

## 另請參閱 {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
