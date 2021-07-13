---
description: 所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
solution: Experience Manager
title: 輔助技術支援
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片，協助工具
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色`region`和`aria-label`屬性預設會設為檢視器的名稱。 可以使用`Container.LABEL`本地化符號控制標籤。

按鈕具有角色`button`和使用`aria-label`屬性設定的描述性文本。 從按鈕的本地化符號的值中填入`aria-label`屬性的值。 禁用按鈕時，將相應設定`aria-disabled`屬性。

滑桿元件具有`slider`角色，具有`aria-valuenow`、`aria-valuemin`和`aria-valuemax`屬性，以描述當前滑桿位置。

縮圖的角色`dialog`，其`aria-label`屬性由`ThumbnailGridView.LABEL`本地化符號控制。 個別縮圖的角色為`button`。 如果已選取縮圖，則會將`aria-selected`屬性設為`true`。

顯示色票的元件具有角色`listbox`，其`aria-label`屬性設定為該元件的`LABEL`本地化符號的值。 個別色票具有`aria-setsize`和`aria-posinset`屬性的角色`option`，以說明集合中的色票位置。 如果選取了色票，則會將`aria-selected`屬性設為`true`。

下拉清單由參考實際下拉式面板元素的附加`aria-haspopup`屬性設為`true`和`aria-controls`屬性的按鈕來啟動。 下拉式面板本身具有角色`menu`，其子元素具有角色`menuitem`。 每個菜單項都指定了`aria-label`屬性。

強制回應對話方塊的角色為`dialog`。 `aria-labelledby`屬性引用了對話框的標題元素。
