---
description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
seo-description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
seo-title: 輔助技術支援
solution: Experience Manager
title: 輔助技術支援
uuid: 9de323c9-d383-41e9-ae44-06600f44a85e
feature: Dynamic Media經典，檢視器，SDK/API，內嵌縮放，協助工具
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---


# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色`region`和`aria-label`屬性預設為檢視器名稱。 您可以使用`Container.LABEL`本地化符號來控制標籤。

主視圖具有`application`角色。 在`aria-roledescription`中提供了主視圖的簡要說明，其值由相應主視圖元件的`ROLE_DESCRIPTION`本地化符號定義。 使用`aria-describedby`提供鍵盤使用者的導覽提示，使用提示的文字來自`USAGE_HINT`本地化符號。 如果資產在「UserData」（用戶資料）欄位中定義了標籤，則`aria-label`屬性將設定為該標籤的值。

顯示色票的元件具有角色`listbox`，且`aria-label`屬性設定為該元件的`LABEL`本地化符號值。 個別色票具有`aria-setsize`和`aria-posinset`屬性的角色`option`，以說明色票在集合中的位置。 如果選擇了色票，則會將`aria-selected`屬性設定為`true`。
