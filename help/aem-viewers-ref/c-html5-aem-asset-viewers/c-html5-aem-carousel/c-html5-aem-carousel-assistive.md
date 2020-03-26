---
description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
seo-description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
seo-title: 輔助技術支援
solution: Experience Manager
title: 輔助技術支援
topic: Dynamic media
uuid: 72b414f4-b647-4afa-a409-a8ba90227d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色 `region` 和屬 `aria-label` 性預設會設為檢視器的名稱。 您可以使用本地化符號來控 `Container.LABEL` 制標籤。

按鈕的角色和描 `button` 述性文字已與屬性 `aria-label` 一起設定。 屬性的 `aria-label` 值由按鈕的本地化符號值填入。 當按鈕停用時，會 `aria-disabled` 相應地設定屬性。

可讓您在轉盤投影片中導覽的按鈕，標籤會根據目前選取的投影片在執行時期更新。 這些按鈕標籤的範本會以本地化符號 `CAROUSELVIEWER_TOOLTIP_GOTO` 設定。

主視圖具有角色 `application`。 文中對主視圖作了簡要描述 `aria-roledescription`，其值由對應主視圖組 `ROLE_DESCRIPTION` 件的本地化符號定義。 鍵盤使用者的導覽提示是使用 `aria-describedby`的，使用提示的文字來自本地化 `USAGE_HINT` 符號。 如果資產在「用戶資料」欄位中定義了標籤，則 `aria-label` 會使用該標籤的值設定屬性。

作用點、區域和影像地圖的角色和描述 `button` 性文字會與屬性 `aria-label` 一起設定，並具有作用點或影像地表徵圖簽的值。 當用戶將焦點放在熱點或影像地圖上時，使用為鍵盤用戶提供導航提示 `aria-describedby`，並且用於使用提示的文本來自本地化 `USAGE_HINT` 符號。
