---
description: 「影像演算」會將材質套用至暈映中的群組或物件。
solution: Experience Manager
title: 材料
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# 材料{#materials}

「影像演算」會將材質套用至暈映中的群組或物件。

材料由一組&#x200B;*屬性*&#x200B;組成。 某些屬性是特定材料的必需屬性，其它屬性是可選的，有些屬性則忽略（如果存在）。 許多屬性都有預設值。 並非所有材料都可應用於所有物體（例如，櫃子材料不能應用於沙發）。

伺服器將忽略發生在「材料規範段」(MSS)中但未列在上面或下面特定材料表中的任何屬性。

下表列出了基本材料屬性。 IR支援控制[高級渲染效果的其他屬性](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)。

除非另有說明，否則所有材料屬性都是可選的，具有合適的預設值。

* [純色](r-ir-solid-colors.md)
* [可重複的紋理](r-ir-repeatable-textures.md)
* [牆邊界](r-ir-wall-borders.md)
* [Decals](r-ir-decals.md)
* [封包](r-ir-cabinets.md)
* [窗口覆蓋](r-ir-window-coverings.md)
