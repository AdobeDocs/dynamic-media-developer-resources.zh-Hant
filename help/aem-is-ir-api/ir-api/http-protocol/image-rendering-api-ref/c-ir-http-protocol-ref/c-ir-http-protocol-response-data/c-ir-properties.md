---
description: 屬性資料會回應下列req= types imageprops和props。
solution: Experience Manager
title: 屬性
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 4%

---


# 屬性{#properties}

屬性資料會回應下列req=類型：imageprops和props。

回覆資料的格式化為可讀為Java屬性。 典型的文本屬性響應具有以下一般結構：

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` 可以是空的。在每行的開始和結束處以及&#39;=&#39;分隔符的前後，空格是可選的。 單引號或雙引號可用來圈住字串值，但不是必要的。

字串值可能包含JAVA樣式的轉義字元，例如`\n`、`\t`、`\:`。 或 `\\`.

**另請參閱**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
