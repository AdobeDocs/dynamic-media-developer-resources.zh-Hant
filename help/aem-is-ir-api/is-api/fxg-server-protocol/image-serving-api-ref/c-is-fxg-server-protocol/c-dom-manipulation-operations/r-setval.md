---
title: setVal
description: 設定s7 elementID的文位元組點值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 1%

---

# setVal{#setval}

設定s7：elementID的文位元組點值。

`setVal.elementID= *[!DNL value]*`

如果FXG節點元素已定義`s7:elementID`，則可以操作該節點的文字值。

## 範例 {#section-f574fd66dedd4a219aa537d7bdabea23}

假設已為`TextGraphic`節點定義`s7:elementID="paragraph1"`屬性，則下列專案有效：

`&setVal.paragraph=Hello`

此範例將段落節點的文字值設為「Hello」。
