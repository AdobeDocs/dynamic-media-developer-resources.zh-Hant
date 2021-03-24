---
description: 將屬性設定為FXG根元素。
solution: Experience Manager
title: setAttr.rootElement
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 1%

---


# setAttr.rootElement{#setattr-rootelement}

將屬性設定為FXG根元素。

` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

此命令可操作根元素的屬性。

## 範例 {#section-2758a6e316c34b99b13b02147e5973bb}

如果我們有下列根元素：

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

應用以下命令後：

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

根元素現在變更為：

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">`
