---
description: 所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
solution: Experience Manager
title: 輔助技術支援
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---


# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的Rich Internet Applications）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色`region`和`aria-label`屬性預設為檢視器名稱。 您可以使用`Container.LABEL`本地化符號來控制標籤。

按鈕具有`button`角色，並使用`aria-label`屬性設定描述性文字。 `aria-label`屬性的值是從按鈕的本地化符號值填入的。 禁用按鈕時，將相應地設定`aria-disabled`屬性。

主視圖具有`application`角色。 在`aria-roledescription`中提供了主視圖的簡要說明，其值由相應主視圖元件的`ROLE_DESCRIPTION`本地化符號定義。 使用`aria-describedby`提供鍵盤使用者的導覽提示，使用提示的文字來自`USAGE_HINT`本地化符號。 如果資產在「UserData」（用戶資料）欄位中定義了標籤，則`aria-label`屬性將設定為該標籤的值。
