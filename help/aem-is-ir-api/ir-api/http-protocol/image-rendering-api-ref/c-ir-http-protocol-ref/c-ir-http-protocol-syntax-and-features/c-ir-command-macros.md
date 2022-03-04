---
title: 命令宏
description: 命令宏提供一組命令的命名快捷方式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# 命令宏{#command-macros}

命令宏提供一組命令的命名快捷方式。

`$ *[!DNL name]*$`

** *[!DNL name]* **宏名稱

宏在單獨的宏定義檔案中定義，這些檔案可附加到材料目錄或預設目錄。

*[!DNL name]* 不區分大小寫，可以由ASCII字母、數字、「 — 」、「_」和「。」的任意組合組成 字元.

在「？」之後的請求中的任何位置或請求中的任何位置調用宏 `vignette::Modifier` 的子菜單。 宏只能表示一個或多個「影像呈現」命令，並且必須與具有「&amp;」分隔符的其他命令分開。

宏調用在分析時被其替換字串提前替換。 如果宏中的命令在請求中調用宏之前發生，則宏中的命令會覆蓋請求中的相同命令。 此工作流與 `vignette::Modifier`，其中請求字串中的命令會覆蓋 `vignette::Modifier` 字串，而不考慮請求中的位置。

命令宏不能具有參數值，但可以使用自定義變數將值從請求傳遞到宏。

宏可能不嵌套。

**範例**

如果將相同的命令或屬性應用於不同的渲染影像，則宏將非常有用。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

您可以為公共屬性定義宏：

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

宏的使用方式如下：

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

因為 `qlt=` 對於第三個請求不同，在調用宏後軟體將覆蓋值(指定 `qlt=` *先* `$render$`無效)。

**另請參閱**

`catalog::MacroFile`。 `catalog::Modifier`，宏定義引用

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
