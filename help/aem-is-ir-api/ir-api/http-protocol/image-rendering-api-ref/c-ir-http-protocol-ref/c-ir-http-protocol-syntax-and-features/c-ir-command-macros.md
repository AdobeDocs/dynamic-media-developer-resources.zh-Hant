---
description: 命令宏為一組命令提供了命名的快捷方式。
solution: Experience Manager
title: 命令宏*
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 1%

---

# 命令宏*{#command-macros}

命令宏為一組命令提供了命名的快捷方式。

`$ *[!DNL name]*$`

** *[!DNL name]* **宏名稱

宏在單獨的宏定義檔案中定義，這些檔案可附加到材料目錄或預設目錄。

*[!DNL name]* 不區分大小寫，並且可以包含ASCII字母、數字、「 — 」、「_」和「」的任意組合。字元.

在「？」後，或在`vignette::Modifier`欄位內的任意位置調用請求中的宏。 宏只能表示一個或多個完整的影像呈現命令，並且必須與具有「&amp;」分隔符的其他命令分開。

在解析期間，宏調用會被其替代字串替換。 如果宏中的命令在請求中的宏調用之前發生，則宏中的命令會覆蓋請求中的相同命令。 這與`vignette::Modifier`不同，後者要求字串中的命令一律會覆寫`vignette::Modifier`字串中的命令，無論要求中的位置為何。

命令巨集不能有引數值，但可使用自訂變數將值從請求傳遞至巨集。

宏不能嵌套。

**範例**

如果將相同的命令或屬性應用於不同的渲染影像，則宏將非常有用。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

您可以為通用屬性定義巨集：

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

宏的使用方式如下：

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

由於第三個請求的`qlt=`不同，因此我們只需在叫用巨集後覆寫值（在&#x200B;*`$render$`之前指定`qlt=`*&#x200B;將不會產生任何效果）。

**另請參閱**

`catalog::MacroFile`,，宏 `catalog::Modifier`定義引用

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
