---
title: 輔助技術支援
description: 所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout,Accessibility
role: Developer,User
exl-id: 0f96939b-0ecc-4d4d-a084-60b023b2a5f2
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素具有角色 `region` 和 `aria-label` 屬性，預設為檢視器的名稱。 您可以使用 `Container.LABEL` 本地化符號。

按鈕具有角色 `button` 和描述性文字集 `aria-label` 屬性。 的值 `aria-label` 屬性是從按鈕的本地化符號的值填入。 當按鈕停用時， `aria-disabled` 屬性已相應設定。

主視圖具有角色 `application`. 主要檢視的簡短說明位於 `aria-roledescription`，而值由 `ROLE_DESCRIPTION` 相應主視圖元件的本地化符號。 為鍵盤用戶提供導航提示，使用 `aria-describedby`，則使用提示的文字來自 `USAGE_HINT` 本地化符號。 如果資產在UserData欄位中定義了標籤，則 `aria-label` 屬性是以此類標籤的值設定。

顯示色票的元件具有角色 `listbox` with `aria-label` 屬性設為的值 `LABEL` 該元件的本地化符號。 個別色票具有角色 `option` with `aria-setsize` 和 `aria-posinset` 屬性，以說明集合中的色票位置。 如果選取了色票，則會取得 `aria-selected` 屬性設定為 `true`.
