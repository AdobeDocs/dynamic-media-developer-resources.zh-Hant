---
description: 屬性資料會回應下列req=類型imageprop和prop。
solution: Experience Manager
title: 屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---

# 屬性{#properties}

屬性資料會回應下列請求類型：imageprop和prop。

回覆資料的格式可讀為Java屬性。 典型文本屬性響應具有以下一般結構：

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` 可以是空的。每行的開頭和結尾以及「=」分隔符前後的空白字元為選用字元。 單引號或雙引號可用來括住字串值，但並非必要項目。

字串值可能包含JAVA樣式的逸出字元，如`\n`、`\t`、`\:`。 或 `\\`.

**另請參閱**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
