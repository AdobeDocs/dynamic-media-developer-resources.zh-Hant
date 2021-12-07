---
title: 輔助技術支援
description: 所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素具有角色 `region` 和 `aria-label` 屬性，預設為檢視器的名稱。 您可以使用 `Container.LABEL` 本地化符號。

按鈕具有角色 `button` 描述性文字集 `aria-label` 屬性。 的值 `aria-label` 屬性是從按鈕的本地化符號的值填入。 按鈕停用時， `aria-disabled` 屬性已相應設定。

滑桿元件具有角色 `slider` 使用屬性 `aria-valuenow`, `aria-valuemin`，和 `aria-valuemax` 來描述當前滑塊位置。

下拉清單由按鈕啟動，其他按鈕 `aria-haspopup` 屬性設定為 `true` 和 `aria-controls` 屬性，此屬性參考實際的下拉式面板元素。 下拉式面板本身有角色 `menu` 具有角色的子元素 `menuitem`. 每個功能表項目都有 `aria-label` 屬性。

強制回應對話方塊具有角色 `dialog`. 對話方塊的標題元素由 `aria-labelledby` 屬性。
