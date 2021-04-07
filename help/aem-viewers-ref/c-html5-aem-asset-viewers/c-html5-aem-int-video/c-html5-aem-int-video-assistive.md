---
description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
solution: Experience Manager
title: 輔助技術支援
feature: Dynamic Media經典，檢視器，SDK/API，互動式視訊，協助功能
role: 開發人員，商業從業人員
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色`region`和`aria-label`屬性預設為檢視器名稱。 您可以使用`Container.LABEL`本地化符號來控制標籤。

按鈕具有`button`角色，並以`aria-label`屬性設定描述性文字。 `aria-label`屬性的值是從按鈕的本地化符號值填入的。 禁用按鈕時，將相應設定`aria-disabled`屬性。

滑塊元件具有`slider`角色，其屬性`aria-valuenow`、`aria-valuemin`和`aria-valuemax`用於描述當前滑塊位置。

縮圖的角色`dialog`,`aria-label`屬性由`ThumbnailGridView.LABEL`本地化符號控制。 個別縮圖具有角色`button`。 如果選取縮圖，則會將`aria-selected`屬性設為`true`。

顯示色票的元件具有角色`listbox`，且`aria-label`屬性設定為該元件的`LABEL`本地化符號值。 個別色票具有`aria-setsize`和`aria-posinset`屬性的角色`option`，以說明色票在集合中的位置。 如果選擇了色票，則會將`aria-selected`屬性設定為`true`。

下拉式清單是由其他`aria-haspopup`屬性設為`true`和`aria-controls`屬性參照實際下拉式面板元素的按鈕所啟動。 下拉式面板本身具有角色`menu`，子元素具有角色`menuitem`。 每個菜單項都指定了`aria-label`屬性。

「模態」對話框具有`dialog`角色。 對話框的標題元素由`aria-labelledby`屬性引用。
