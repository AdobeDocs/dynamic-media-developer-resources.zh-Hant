---
description: 命令宏為命令集提供命名快捷方式。
seo-description: 命令宏為命令集提供命名快捷方式。
seo-title: 命令宏*
solution: Experience Manager
title: 命令宏*
topic: Scene7 Image Serving - Image Rendering API
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 命令宏*{#command-macros}

命令宏為命令集提供命名快捷方式。

`$ *[!DNL name]*$`

** *[!DNL name]* **宏名稱

宏定義在單獨的宏定義檔案中，這些宏可附加到材料目錄或預設目錄。

*[!DNL name]* 不區分大小寫，且可包含任何ASCII字母、數字、&#39;-&#39;、&#39;_&#39;和&#39;.&#39;的組合 字元.

在&#39;?&#39;後的任何位置或欄位中的任何位置叫用 `vignette::Modifier` 巨集。 宏只能表示一個或多個完整的影像渲染命令，並且必須與具有「&amp;」分隔符的其他命令分開。

宏調用在解析期間早被其替代字串替換。 如果宏中的命令在請求中調用宏之前發生，則會覆蓋請求中的相同命令。 這與請求字 `vignette::Modifier`串中的命令一律會覆寫字串中的命令不同，不 `vignette::Modifier` 論請求在何處。

命令宏不能有參數值，但可使用自定義變數將值從請求傳遞到宏。

宏可能不嵌套。

**範例**

如果要將相同的命令或屬性應用於不同的渲染影像，宏就很有用。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

可以為公共屬性定義宏：

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

宏的用法如下：

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

由於 `qlt=` 第三個請求不同，我們只會在呼叫巨集後覆寫值(指定 `qlt=`*之&#x200B;*`$render$`前不會有任何效果)。

**另請參閱**

`catalog::MacroFile`、 `catalog::Modifier`，宏定義參考

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

