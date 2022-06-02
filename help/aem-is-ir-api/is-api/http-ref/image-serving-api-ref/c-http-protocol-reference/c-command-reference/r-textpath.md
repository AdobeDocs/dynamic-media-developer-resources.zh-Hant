---
title: 文本路徑
description: 文本路徑。 指定用作隨textPs=提供的文本的基線的路徑。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# 文本路徑{#textpath}

文本路徑。 指定用作隨textPs=提供的文本的基線的路徑。

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
</table>

請參閱 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 有關其他資訊，包括 *`pathDefinition`*。

>[!NOTE]
>
>不同於 `clipPath=`，在子路徑的末尾未指定「z」或「Z」時，不會自動關閉文本路徑。

*`pathDefinition`* 可能包括多個子路徑。 文本按指定的順序呈現在子路徑上。

RTF命令 `\ql`。 `\qc`。 `\qr`。 `\li`, `\ri` 可用於沿路徑定位渲染的文本。

## 屬性 {#section-068137df436c46b9b55d271eb60e7285}

文本層屬性( `textPs=` 僅)。 被其他層忽略。 應用於 `layer=0` 如果指定 `layer=comp`。 如果忽略 `textPs=` 。

如果圖層同時包含這兩者，則返回錯誤 `textPath=` 和 `textFlowPath=`。

## 預設 {#section-697b1f2cfc43498080a31327e6eb173d}

無，用於標準文本呈現。

## 另請參閱 {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) 。 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)。 [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)。 [文本圖層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
