---
description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
solution: Experience Manager
title: 輔助技術支援
feature: Dynamic Media經典，檢視器，SDK/API，互動式影像，協助功能
role: 開發人員，商業從業人員
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色`region`和`aria-label`屬性預設為檢視器名稱。 您可以使用`Container.LABEL`本地化符號來控制標籤。

主視圖具有`application`角色。 在`aria-roledescription`中提供了主視圖的簡要說明，其值由相應主視圖元件的`ROLE_DESCRIPTION`本地化符號定義。 使用`aria-describedby`提供鍵盤使用者的導覽提示，使用提示的文字來自`USAGE_HINT`本地化符號。 如果資產在「UserData」（用戶資料）欄位中定義了標籤，則`aria-label`屬性將設定為該標籤的值。

作用點、區域和影像地圖具有角色`button`和描述性文字集（具有`aria-label`屬性），且具有作用點或影像地表徵圖簽的值。 當用戶將焦點放在熱點或影像地圖上時，使用`aria-describedby`為鍵盤用戶提供導航提示，其中使用提示的文本來自`USAGE_HINT`本地化符號。
