---
title: 輔助技術支援
description: 所有查看器元件都支援ARIA（可訪問的富網際網路應用程式）角色和屬性，以改進與輔助技術（如螢幕閱讀器）的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有查看器元件都支援ARIA（可訪問的富網際網路應用程式）角色和屬性，以改進與輔助技術（如螢幕閱讀器）的整合。

頂級查看器元素具有角色 `region` 和 `aria-label` 預設設定為查看器名稱的屬性。 可以使用 `Container.LABEL` 本地化符號。

按鈕具有角色 `button` 和描述性文本集 `aria-label` 屬性。 值 `aria-label` 屬性是從按鈕的本地化符號的值填充的。 當按鈕被禁用時， `aria-disabled` 屬性被相應設定。

主視圖具有角色 `application`。 中提供了主視圖的簡要說明 `aria-roledescription`，其值由 `ROLE_DESCRIPTION` 相應主視圖元件的本地化符號。 為鍵盤用戶提供導航提示時使用 `aria-describedby`，使用提示的文本來自 `USAGE_HINT` 本地化符號。 如果資產在UserData欄位中定義了標籤， `aria-label` 屬性是使用此類標籤的值設定的。

熱點、區域和影像映射具有作用 `button` 描述性文本集 `aria-label` 屬性，以及熱點或影像映射標籤的值。 當用戶將焦點放在熱點或影像地圖上時，使用 `aria-describedby`，其中使用提示的文本來自 `USAGE_HINT` 本地化符號。

縮略圖具有角色 `dialog` 與 `aria-label` 由控制的屬性 `ThumbnailGridView.LABEL` 本地化符號。 單個縮略圖具有角色 `button`。 如果選擇了縮略圖，則會獲得 `aria-selected` 屬性集 `true`。

顯示色板的元件具有角色 `listbox` 與 `aria-label` 屬性設定為 `LABEL` 該元件的本地化符號。 單個色板具有角色 `option` 與 `aria-setsize` 和 `aria-posinset` 屬性，用於描述集中的色板位置。 如果選取了色板，則會獲取 `aria-selected` 屬性集 `true`。

下拉清單由帶有附加項的按鈕激活 `aria-haspopup` 屬性集 `true` 和 `aria-controls` 引用實際下拉面板元素的屬性。 下拉面板本身具有角色 `menu` 具有角色的子元素 `menuitem`。 每個菜單項都 `aria-label` 已指定屬性。

「模式」(Modal)對話框具有角色 `dialog`。 對話框的頭元素由 `aria-labelledby` 屬性。
