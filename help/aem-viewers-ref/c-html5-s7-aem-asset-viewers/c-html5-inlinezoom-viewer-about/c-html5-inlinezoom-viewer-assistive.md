---
description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
seo-description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
seo-title: 輔助技術支援
solution: Experience Manager
title: 輔助技術支援
topic: Dynamic media
uuid: 9de323c9-d383-41e9-ae44-06600f44a85e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色 `region` 和屬 `aria-label` 性預設會設為檢視器的名稱。 您可以使用本地化符號來控 `Container.LABEL` 制標籤。

主視圖具有角色 `application`。 文中對主視圖作了簡要描述 `aria-roledescription`，其值由對應主視圖 `ROLE_DESCRIPTION` 元件的本地化符號定義。 鍵盤使用者的導覽提示是使用 `aria-describedby`的，使用提示的文字來自本地化 `USAGE_HINT` 符號。 如果資產在「用戶資料」欄位中定義了標籤，則 `aria-label` 會使用該標籤的值設定屬性。

顯示色票的元件具有角色， `listbox` 其屬 `aria-label` 性設定為該元件的本 `LABEL` 地化符號的值。 個別色票具有角 `option` 色和 `aria-setsize` 屬 `aria-posinset` 性，可描述色票在集合中的位置。 如果選取了色票，則會將屬 `aria-selected` 性設為 `true`。
