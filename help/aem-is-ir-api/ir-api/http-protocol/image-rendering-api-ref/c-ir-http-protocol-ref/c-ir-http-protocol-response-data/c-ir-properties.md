---
title: 屬性
description: 屬性資料會傳回，以回應下列req=型別imageprop和prop。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
TQID: 'https://experienceleague.adobe.com/AIeKRT2-o9Z35SjXjrGECIWHFLRrdJz5JO-CkCOLj8U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 100
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

