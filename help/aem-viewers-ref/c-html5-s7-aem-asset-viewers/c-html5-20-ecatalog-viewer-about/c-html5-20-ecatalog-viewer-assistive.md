---
description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
seo-description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
seo-title: 輔助技術支援
solution: Experience Manager
title: 輔助技術支援
topic: Dynamic media
uuid: 8565383e-5c13-4af0-9b6e-2d583c18f19c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色 `region` 和屬 `aria-label` 性預設會設為檢視器的名稱。 您可以使用本地化符號來控 `Container.LABEL` 制標籤。

按鈕具有與屬 `button` 性一起設定的角色和描述 `aria-label` 性文本。 屬性的 `aria-label` 值由按鈕的本地化符號值填入。 當按鈕停用時，屬性 `aria-disabled` 會隨之設定。

主視圖具有角色 `application`。 文中對主視圖作了簡要描述 `aria-roledescription`，其值由對應主視圖組 `ROLE_DESCRIPTION` 件的本地化符號定義。 鍵盤使用者的導覽提示是使用 `aria-describedby`的，使用提示的文字來自本地化 `USAGE_HINT` 符號。 如果資產在「用戶資料」欄位中定義了標籤，則 `aria-label` 會使用該標籤的值設定屬性。

作用點、區域和影像地圖的角色和描述 `button` 性文字會與屬性 `aria-label` 一起設定，並具有作用點或影像地表徵圖簽的值。 當用戶將焦點放在熱點或影像地圖上時，使用為鍵盤用戶提供導航提示 `aria-describedby`，並且用於使用提示的文本來自本地化 `USAGE_HINT` 符號。

縮圖具有由本地 `dialog` 化符 `aria-label` 號控制的屬性 `ThumbnailGridView.LABEL` 的角色。 個別縮圖具有角色 `button`。 如果選取縮圖，則會將屬 `aria-selected` 性設為 `true`。

顯示色票的元件具有角色， `listbox` 其屬 `aria-label` 性設定為該元件的本 `LABEL` 地化符號的值。 個別色票具有角 `option` 色和 `aria-setsize` 屬 `aria-posinset` 性，可描述色票在集合中的位置。 如果選取了色票，則會將屬 `aria-selected` 性設為 `true`。

下拉式清單是由將其他屬性設 `aria-haspopup` 為的按鈕和引 `true` 用 `aria-controls` 實際下拉式面板元素的屬性來啟動。 下拉式面板本身具有角色， `menu` 而子元素具有角色 `menuitem`。 每個功能表項目都有指 `aria-label` 定的屬性。

模態對話框具有角色 `dialog`。 該屬性引用了該對話框的標題 `aria-labelledby` 元素。
