---
description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
solution: Experience Manager
title: 輔助技術支援
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---


# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色`region`和`aria-label`屬性預設為檢視器名稱。 您可以使用`Container.LABEL`本地化符號來控制標籤。

按鈕具有`button`角色，並使用`aria-label`屬性設定描述性文字。 `aria-label`屬性的值是從按鈕的本地化符號值填入的。 禁用按鈕時，將相應地設定`aria-disabled`屬性。

主視圖具有`application`角色。 在`aria-roledescription`中提供了主視圖的簡要說明，其值由相應主視圖元件的`ROLE_DESCRIPTION`本地化符號定義。 使用`aria-describedby`提供鍵盤使用者的導覽提示，使用提示的文字來自`USAGE_HINT`本地化符號。 如果資產在「UserData」（用戶資料）欄位中定義了標籤，則`aria-label`屬性將設定為該標籤的值。

作用點、區域和影像地圖具有角色`button`和描述性文字集（具有`aria-label`屬性），且具有作用點或影像地表徵圖簽的值。 當用戶將焦點放在熱點或影像地圖上時，使用`aria-describedby`為鍵盤用戶提供導航提示，其中使用提示的文本來自`USAGE_HINT`本地化符號。

縮圖的角色`dialog`,`aria-label`屬性由`ThumbnailGridView.LABEL`本地化符號控制。 個別縮圖具有角色`button`。 如果選取縮圖，則會將`aria-selected`屬性設為`true`。

顯示色票的元件具有角色`listbox`，且`aria-label`屬性設定為該元件的`LABEL`本地化符號值。 個別色票具有`aria-setsize`和`aria-posinset`屬性的角色`option`，以說明色票在集合中的位置。 如果選擇了色票，則會將`aria-selected`屬性設定為`true`。

下拉式清單是由其他`aria-haspopup`屬性設為`true`的按鈕和參照實際下拉式面板元素的`aria-controls`屬性來啟動。 下拉式面板本身具有角色`menu`，子元素具有角色`menuitem`。 每個菜單項都指定了`aria-label`屬性。

「模態」對話框具有`dialog`角色。 對話框的標題元素由`aria-labelledby`屬性引用。
