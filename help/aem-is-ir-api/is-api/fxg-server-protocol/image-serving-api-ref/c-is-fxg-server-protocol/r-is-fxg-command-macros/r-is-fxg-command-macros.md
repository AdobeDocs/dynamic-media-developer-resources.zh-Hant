---
title: 指令巨集
description: 指令巨集為指令集提供已命名的捷徑。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# 指令巨集{#command-macros}

指令巨集為指令集提供已命名的捷徑。

巨集是在個別的巨集定義檔案中定義，這些檔案可附加到影像目錄或預設目錄。

巨集可在&#39;？&#39;之後的任何要求中叫用，也可在`catalog::Modifier`欄位內的任何地方叫用。 巨集只能代表一或多個完整的「影像伺服」命令，因此必須以「&amp;」分隔符號括住（修飾元字串的開頭或結尾除外）。

在剖析期間，巨集引動詞在早期會被替代字串取代。 巨集內的命令會覆寫請求中的相同命令（如果這些命令發生在請求中的巨集呼叫之前）。 此流程不同於`catalog::Modifier`，其要求字串中的命令一律會覆寫`catalog::Modifier`字串中的命令，無論要求中的位置為何。

巨集可以巢狀化。 不過，只有在巨集定義剖析時已定義巨集時，才能叫用巨集。 此流程可透過先前在相同巨集定義檔案中顯示，或將此類內嵌巨集的定義置於預設巨集定義檔案中來完成。

如果要將相同的屬性套用至不同的影像，巨集就相當有用。

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

您可以定義通用屬性的巨集：

`view wid=240&fmt=pdf&imageRes=300`

巨集的使用方式如下：

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

因為第三個要求的`wid=`不同，您只需覆寫&#x200B;*after*&#x200B;值，就會叫用巨集（指定`wid=` *before* `$view$`無效）。

+ [name](r-name.md)
