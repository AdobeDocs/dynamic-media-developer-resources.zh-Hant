---
title: setVal
description: 設定s7 elementID的文位元組點值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
TQID: 'https://experienceleague.adobe.com/bwE12rWee56rVQDuctPsmq5TUwVJy39HNUff-ZYuybM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 1%

---

# setVal{#setval}

設定s7:elementID的文位元組點值。

`setVal.elementID= *[!DNL value]*`

如果FXG節點元素已定義`s7:elementID`，則可以操作該節點的文字值。

## 範例 {#section-f574fd66dedd4a219aa537d7bdabea23}

假設已為`TextGraphic`節點定義`s7:elementID="paragraph1"`屬性，則下列專案有效：

`&setVal.paragraph=Hello`

此範例將段落節點的文字值設為「Hello」。
