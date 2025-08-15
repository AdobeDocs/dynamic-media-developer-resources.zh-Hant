---
title: 文字路徑
description: 文字路徑。 指定要用來作為textPs=所提供之文字的基準的路徑。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# 文字路徑{#textpath}

文字路徑。 指定要用來作為textPs=所提供之文字的基準的路徑。

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
</table>

請參閱[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)以取得其他資訊，包括&#x200B;*`pathDefinition`*&#x200B;的說明。

>[!NOTE]
>
>與`clipPath=`不同，當子路徑的結尾未指定&#39;z&#39;或&#39;Z&#39;時，文字路徑不會自動關閉。

*`pathDefinition`*&#x200B;可能包含多個子路徑。 文字會依照指定的順序在子路徑上轉譯。

RTF命令`\ql`、`\qc`、`\qr`、`\li`和`\ri`可用來沿著路徑定位轉譯的文字。

## 屬性 {#section-068137df436c46b9b55d271eb60e7285}

文字圖層屬性（僅限`textPs=`）。 被其他圖層忽略。 若指定給`layer=0`，則套用至`layer=comp`。 如果`textPs=`存在，則忽略。

如果圖層同時包含`textPath=`和`textFlowPath=`，則會傳回錯誤。

## 預設 {#section-697b1f2cfc43498080a31327e6eb173d}

無，用於標準文字轉譯。

## 另請參閱 {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ， [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)， [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)， [文字圖層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
