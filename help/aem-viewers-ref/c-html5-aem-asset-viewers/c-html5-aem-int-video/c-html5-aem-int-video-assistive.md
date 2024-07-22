---
title: 輔助技術支援
description: 所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。

最上層檢視器元素具有角色`region`和`aria-label`屬性，預設設定為檢視器的名稱。 您可以使用`Container.LABEL`本地化符號控制標籤。

按鈕具有角色`button`和描述性文字設定了`aria-label`屬性。 `aria-label`屬性的值是從按鈕本地化符號的值填入的。 當按鈕停用時，會相應設定`aria-disabled`屬性。

Slider元件具有屬性`aria-valuenow`、`aria-valuemin`和`aria-valuemax`的角色`slider`可描述目前的Slider位置。

縮圖具有角色`dialog`，其屬性為`aria-label`，由`ThumbnailGridView.LABEL`本地化符號控制。 個別縮圖具有角色`button`。 如果選取縮圖，它將取得`aria-selected`屬性設定為`true`。

顯示色票的元件具有角色`listbox`，`aria-label`屬性設定為該元件的`LABEL`本地化符號的值。 個別色票具有`aria-setsize`和`aria-posinset`屬性的角色`option`，可說明色票在集中的位置。 如果選取色票，則會將`aria-selected`屬性設定為`true`。

下拉式清單由按鈕啟動，按鈕具有設定為`true`的其他`aria-haspopup`屬性以及參考實際下拉式面板專案的`aria-controls`屬性。 下拉式面板本身具有角色`menu`，其子元素具有角色`menuitem`。 每個功能表專案都指定了`aria-label`屬性。

模型對話方塊具有角色`dialog`。 對話方塊的標頭專案由`aria-labelledby`屬性參考。
