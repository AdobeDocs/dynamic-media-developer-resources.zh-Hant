---
title: 材料
description: 「影像渲染」(Image Rendering)將材料應用於小格中的組或對象。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# 材料{#materials}

「影像渲染」(Image Rendering)將材料應用於小格中的組或對象。

材料由一組 *屬性*。 某些材料需要某些屬性，其他屬性是可選的，如果存在，則忽略某些屬性。 許多屬性都具有預設值。 並非所有材料都可應用於所有對象（例如，櫥櫃材料不能應用於沙發）。

在「材料規範段」(MSS)中出現但未在上面或下面的特定材料表中列出的任何屬性，伺服器將忽略。

下表列出了基本材料屬性。 IR支援用於控制的附加屬性 [高級渲染效果](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)。

除非另有說明，否則所有材料屬性都是可選的，並且具有合適的預設值。

* [純色](r-ir-solid-colors.md)
* [可重複的紋理](r-ir-repeatable-textures.md)
* [牆邊界](r-ir-wall-borders.md)
* [貼花](r-ir-decals.md)
* [封包](r-ir-cabinets.md)
* [窗蓋](r-ir-window-coverings.md)
