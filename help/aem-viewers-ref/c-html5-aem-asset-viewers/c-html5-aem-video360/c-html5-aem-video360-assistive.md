---
description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
solution: Experience Manager
title: 輔助技術支援
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊，協助功能
role: 開發人員，商業從業人員
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色`region`和`aria-label`屬性預設為檢視器名稱。 您可以使用`Container.LABEL`本地化符號來控制標籤。

按鈕具有`button`角色，並以`aria-label`屬性設定描述性文字。 `aria-label`屬性的值是從按鈕的本地化符號值填入的。 禁用按鈕時，將相應設定`aria-disabled`屬性。

滑塊元件具有`slider`角色，其屬性`aria-valuenow`、`aria-valuemin`和`aria-valuemax`用於描述當前滑塊位置。

下拉式清單是由其他`aria-haspopup`屬性設為`true`和`aria-controls`屬性參照實際下拉式面板元素的按鈕所啟動。 下拉式面板本身具有角色`menu`，子元素具有角色`menuitem`。 每個菜單項都指定了`aria-label`屬性。

「模態」對話框具有`dialog`角色。 對話框的標題元素由`aria-labelledby`屬性引用。
