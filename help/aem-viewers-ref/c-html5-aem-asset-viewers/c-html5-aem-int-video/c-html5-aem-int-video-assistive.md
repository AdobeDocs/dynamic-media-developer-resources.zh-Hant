---
description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
seo-description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
seo-title: 輔助技術支援
solution: Experience Manager
title: 輔助技術支援
topic: Dynamic media
uuid: 0abed8d4-9754-47b1-9de7-cce665de03b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色 `region` 和屬 `aria-label` 性預設會設為檢視器的名稱。 您可以使用本地化符號來控 `Container.LABEL` 制標籤。

按鈕的角色和描 `button` 述性文字已與屬性 `aria-label` 一起設定。 屬性的 `aria-label` 值由按鈕的本地化符號值填入。 當按鈕停用時，會 `aria-disabled` 相應地設定屬性。

滑桿元件具有具 `slider` 有屬性 `aria-valuenow`的角色 `aria-valuemin`，以及 `aria-valuemax` 描述目前滑桿位置。

縮圖具有由本地 `dialog` 化符 `aria-label` 號控制的屬性 `ThumbnailGridView.LABEL` 的角色。 個別縮圖具有角色 `button`。 如果選取縮圖，則會將屬 `aria-selected` 性設為 `true`。

顯示色票的元件具有角色， `listbox` 其屬 `aria-label` 性設定為該元件的本 `LABEL` 地化符號的值。 個別色票具有角 `option` 色和 `aria-setsize` 屬 `aria-posinset` 性，可描述色票在集合中的位置。 如果選取了色票，則會將屬 `aria-selected` 性設為 `true`。

下拉式清單是由按鈕所啟用，其中 `aria-haspopup` 附加屬性設為 `true``aria-controls` ，屬性參照實際的下拉式面板元素。 下拉式面板本身具有角色， `menu` 而子元素具有角色 `menuitem`。 每個功能表項目都有指 `aria-label` 定的屬性。

模態對話框具有角色 `dialog`。 該屬性引用了該對話框的標題 `aria-labelledby` 元素。
