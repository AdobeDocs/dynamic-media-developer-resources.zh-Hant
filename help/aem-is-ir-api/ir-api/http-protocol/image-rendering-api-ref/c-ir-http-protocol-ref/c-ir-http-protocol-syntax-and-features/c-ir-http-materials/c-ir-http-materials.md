---
description: 影像呈現將材料應用於暈映中的組或對象。
solution: Experience Manager
title: 材料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 材料{#materials}

影像呈現將材料應用於暈映中的組或對象。

材料由一組&#x200B;*屬性*&#x200B;組成。 某些材料需要某些屬性，其他屬性為可選屬性，有些則忽略（如果存在）。 許多屬性都有預設值。 並非所有材料都可應用於所有對象（例如，櫥櫃材料不能應用於沙發）。

伺服器將忽略發生在材料規範段(MSS)內但未列於上面或下面特定材料表中的任何屬性。

下表列出了基本材料屬性。 IR支援控制[高級渲染效果的其他屬性](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)。

除非另有說明，否則所有材料屬性都是可選的，具有適當的預設值。

* [純色](r-ir-solid-colors.md)
* [可重複的紋理](r-ir-repeatable-textures.md)
* [牆邊界](r-ir-wall-borders.md)
* [德卡爾](r-ir-decals.md)
* [封包](r-ir-cabinets.md)
* [窗口覆蓋](r-ir-window-coverings.md)
