---
title: 輔助技術支援
description: 所有查看器元件都支援ARIA（可訪問的富網際網路應用程式）角色和屬性，以改進與輔助技術（如螢幕閱讀器）的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有查看器元件都支援ARIA（可訪問的富網際網路應用程式）角色和屬性，以改進與輔助技術（如螢幕閱讀器）的整合。

頂級查看器元素具有角色 `region` 和 `aria-label` 預設設定為查看器名稱的屬性。 可以使用 `Container.LABEL` 本地化符號。

按鈕具有角色 `button` 描述性文本集 `aria-label` 屬性。 值 `aria-label` 屬性是從按鈕的本地化符號的值填充的。 禁用按鈕時， `aria-disabled` 屬性被相應設定。

滑塊元件具有角色 `slider` 使用屬性 `aria-valuenow`。 `aria-valuemin`, `aria-valuemax` 描述當前滑塊位置。

縮略圖具有角色 `dialog` 與 `aria-label` 由控制的屬性 `ThumbnailGridView.LABEL` 本地化符號。 單個縮略圖具有角色 `button`。 如果選擇了縮略圖，則會獲得 `aria-selected` 屬性集 `true`。

顯示色板的元件具有角色 `listbox` 與 `aria-label` 屬性設定為 `LABEL` 該元件的本地化符號。 單個色板具有角色 `option` 與 `aria-setsize` 和 `aria-posinset` 屬性，用於描述集中的色板位置。 如果選取了色板，則會獲取 `aria-selected` 屬性集 `true`。

下拉清單由帶有附加項的按鈕激活 `aria-haspopup` 屬性集 `true` 和 `aria-controls` 引用實際下拉面板元素的屬性。 下拉面板本身具有角色 `menu` 具有角色的子元素 `menuitem`。 每個菜單項都 `aria-label` 已指定屬性。

「模式」(Modal)對話框具有角色 `dialog`。 對話框的頭元素由 `aria-labelledby` 屬性。
