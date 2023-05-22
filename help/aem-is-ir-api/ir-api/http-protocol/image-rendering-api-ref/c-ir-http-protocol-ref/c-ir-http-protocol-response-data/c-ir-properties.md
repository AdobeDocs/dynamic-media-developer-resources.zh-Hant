---
title: 屬性
description: 響應以下req=類型imageprops和props返回屬性資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---

# 屬性{#properties}

響應以下req=類型返回屬性資料：影像道具和道具。

回復資料的格式設定為可讀為Java™屬性。 典型的文本屬性響應具有以下一般結構：

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` 可以是空的。 在每行的開頭和結尾以及「=」分隔符前後，空格是可選的。 單引號或雙引號可用於引起字串值，但不是必需的。

字串值可能包含JAVA樣式轉義字元，如 `\n`。 `\t`。 `\:`或 `\\`。

**另請參閱**

[請求=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
