---
title: 屬性
description: 屬性資料會傳回，以回應下列req=型別imageprop和prop。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# 屬性{#properties}

屬性資料會傳回以回應下列req=型別： imageprops和props。

回覆資料的格式會設定為Java™屬性以供讀取。 典型的文字屬性回應具有此一般結構：

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*`可以空白。 每行開頭和結尾以及&#39;=&#39;分隔符號前後的空白字元為選用。 單引號或雙引號可用來將字串值括住，但並非必要。

字串值可包含JAVA樣式的逸出字元，例如`\n`、`\t`、`\:`或`\\`。

**另請參閱**

[需要=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
