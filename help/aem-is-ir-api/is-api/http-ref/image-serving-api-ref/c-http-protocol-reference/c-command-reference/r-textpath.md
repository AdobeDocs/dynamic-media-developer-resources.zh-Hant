---
description: 文字路徑。 指定用作文字Ps=所提供之文字基線的路徑。
solution: Experience Manager
title: textPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---


# textPath{#textpath}

文字路徑。 指定用作文字Ps=所提供之文字基線的路徑。

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
</table>

如需詳細資訊，包括&#x200B;*`pathDefinition`*&#x200B;的說明，請參閱[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)。

>[!NOTE]
>
>與`clipPath=`不同，當子路徑結尾未指定&#39;z&#39;或&#39;Z&#39;時，不會自動關閉文字路徑。

*`pathDefinition`* 可能包括多個子路徑。文字會按照指定的順序呈現在子路徑上。

RTF命令`\ql`、`\qc`、`\qr`、`\li`和`\ri`可用於沿路徑定位渲染的文本。

## 屬性 {#section-068137df436c46b9b55d271eb60e7285}

文字圖層屬性（僅限`textPs=`）。 被其他圖層忽略。 如果為`layer=comp`指定，則套用至`layer=0`。 如果`textPs=`存在，則忽略。

如果圖層同時包含`textPath=`和`textFlowPath=`，則會傳回錯誤。

## 預設 {#section-697b1f2cfc43498080a31327e6eb173d}

無，用於標準文本渲染。

## 另請參閱 {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)，文字圖 [層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
