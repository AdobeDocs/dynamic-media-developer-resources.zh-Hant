---
title: 輔助技術支援
description: 所有查看器元件都支援ARIA（可訪問的富網際網路應用程式）角色和屬性，以改進與輔助技術（如螢幕閱讀器）的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: ef2cf58a-bdf0-4136-8d91-692c899cfef7
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有查看器元件都支援ARIA（可訪問的富網際網路應用程式）角色和屬性，以改進與輔助技術（如螢幕閱讀器）的整合。

頂級查看器元素具有角色 `region` 和 `aria-label` 預設設定為查看器名稱的屬性。 可以使用 `Container.LABEL` 本地化符號。

按鈕具有角色 `button` 描述性文本集 `aria-label` 屬性。 值 `aria-label` 屬性是從按鈕的本地化符號的值填充的。 禁用按鈕時， `aria-disabled` 屬性被相應設定。

主視圖具有角色 `application`。 中提供了主視圖的簡要說明 `aria-roledescription`，其值由 `ROLE_DESCRIPTION` 相應主視圖元件的本地化符號。 為鍵盤用戶提供導航提示時使用 `aria-describedby`，使用提示的文本來自 `USAGE_HINT` 本地化符號。 如果資產在UserData欄位中定義了標籤， `aria-label` 屬性是使用此類標籤的值設定的。

顯示色板的元件具有角色 `listbox` 與 `aria-label` 屬性設定為 `LABEL` 該元件的本地化符號。 單個色板具有角色 `option` 與 `aria-setsize` 和 `aria-posinset` 屬性，用於描述集中的色板位置。 如果選取了色板，則會獲取 `aria-selected` 屬性集 `true`。
