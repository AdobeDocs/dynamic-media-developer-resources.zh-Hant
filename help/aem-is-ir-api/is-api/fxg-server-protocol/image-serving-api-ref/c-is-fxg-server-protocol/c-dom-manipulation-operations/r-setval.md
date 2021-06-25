---
description: 為s7 elementID設定文位元組點值。
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---

# setVal{#setval}

為s7:elementID設定文位元組點值。

`setVal.elementID= *[!DNL value]*`

如果FXG節點元素已定義`s7:elementID`，則可操作該節點的文本值。

## 範例 {#section-f574fd66dedd4a219aa537d7bdabea23}

假設已為`TextGraphic`節點定義`s7:elementID="paragraph1"`屬性，則下列內容有效：

`&setVal.paragraph=Hello`

此示例將段落節點的文本值設定為「Hello」。
