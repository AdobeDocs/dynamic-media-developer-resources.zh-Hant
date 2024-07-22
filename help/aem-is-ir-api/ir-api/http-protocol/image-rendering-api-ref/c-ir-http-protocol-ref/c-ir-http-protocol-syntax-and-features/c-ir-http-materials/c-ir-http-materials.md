---
title: 材料
description: 「影像演算」會將材質套用至暈映中的群組或物件。
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

「影像演算」會將材質套用至暈映中的群組或物件。

材質包含一組&#x200B;*屬性*。 某些屬性是某些材料的必要屬性，其他屬性則是選用屬性，有些屬性如果存在則會被忽略。 許多屬性都有預設值。 並非所有材料都可套用至所有物件（例如，無法將檔案櫃材料套用至沙發）。

伺服器會忽略任何出現在「材料規格區段」(MSS)中，但並未列在上方或下方特定材料表格中的屬性。

下表列出基本材料屬性。 IR支援其他屬性來控制[進階演算效果](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)。

除非另有註明，否則所有材料屬性都是選用的，並帶有適當的預設值。

* [純色](r-ir-solid-colors.md)
* [可重複的紋理](r-ir-repeatable-textures.md)
* [牆邊框](r-ir-wall-borders.md)
* [貼花](r-ir-decals.md)
* [檔案櫃](r-ir-cabinets.md)
* [視窗涵蓋範圍](r-ir-window-coverings.md)
