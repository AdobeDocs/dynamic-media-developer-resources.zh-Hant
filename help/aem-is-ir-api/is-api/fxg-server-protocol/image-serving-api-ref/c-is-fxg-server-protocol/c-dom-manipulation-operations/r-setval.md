---
description: 為s7 elementID設定文位元組點值。
seo-description: 為s7 elementID設定文位元組點值。
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Scene7 Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setVal{#setval}

為s7:elementID設定文位元組點值。

`setVal.elementID= *[!DNL value]*`

如果FXG節點元素已定義， `s7:elementID` 則可以處理該節點的文本值。

## 範例 {#section-f574fd66dedd4a219aa537d7bdabea23}

假設已 `s7:elementID="paragraph1"` 為節點定義屬性， `TextGraphic` 則下列內容有效：

`&setVal.paragraph=Hello`

此示例將段落節點的文本值設定為&quot;Hello&quot;。
