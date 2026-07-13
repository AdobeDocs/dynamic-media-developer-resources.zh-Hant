---
title: 指令巨集
description: 指令巨集為指令集提供已命名的捷徑。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
TQID: 'https://experienceleague.adobe.com/cXLJJQ5CS-Apmq-8qYV-ew-lcvfRjoNfIbl2qyyKB6U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# 指令巨集{#command-macros}

指令巨集為指令集提供已命名的捷徑。

`$ *[!DNL name]*$`

**一下&#x200B;*[!DNL name]***巨集名稱

巨集是在單獨的巨集定義檔案中定義的，這些檔案可附加到材料目錄或預設目錄中。

*[!DNL name]*&#x200B;不區分大小寫，並且可以包含ASCII字母、數字、&#39;-&#39;、&#39;_&#39;和&#39;.&#39;字元的任意組合。

在&#39;？&#39;之後的任何要求中或在`vignette::Modifier`欄位中的任何地方叫用巨集。 巨集只能代表一或多個影像演算指令，且必須與其他指令以&#39;&amp;&#39;分隔符號分隔。

在剖析期間，巨集引動詞在早期會被替代字串取代。 巨集內的命令會覆寫請求中的相同命令（如果這些命令發生在請求中的巨集呼叫之前）。 此工作流程不同於`vignette::Modifier`，其要求字串中的命令會覆寫`vignette::Modifier`字串中的命令，無論要求中的位置為何。

命令巨集不能有引數值，但自訂變數可用來將要求中的值傳遞至巨集。

巨集不可巢狀化。

**範例**

如果要將相同的命令或屬性套用到不同的演算影象，巨集就很有用。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

您可以定義通用屬性的巨集：

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

巨集的使用方式如下：

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

因為`qlt=`與第三個要求不同，在呼叫巨集之後，軟體會覆寫值（指定`qlt=` *before* `$render$`無效）。

**另請參閱**

`catalog::MacroFile`，`catalog::Modifier`，巨集定義參考

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

