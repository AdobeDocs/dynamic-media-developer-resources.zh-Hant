---
description: 文本流排除區域。 指定要從文本流中排除的一個或多個區域。
solution: Experience Manager
title: textFlowXPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# textFlowXPath{#textflowxpath}

文本流排除區域。 指定要從文本流中排除的一個或多個區域。

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
</table>

請參閱 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 有關其他資訊，包括 *`pathDefinition`*。 如果未指定路徑定義， `textFlowXPath=` 忽略。

## 屬性 {#section-cd1ebb151d4a405fbfc508d46522d686}

文本層屬性( `textPs=` 僅)。 被其他層忽略，或當指定時 `textFlowPath=`。 應用於 `layer=0` 如果指定 `layer=comp`。

## 預設 {#section-9405cda904684d829ed12a9e40a4dc46}

無。

## 另請參閱 {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) 。 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)。 [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
