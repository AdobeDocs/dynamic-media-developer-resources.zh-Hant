---
title: 輔助技術支援
description: 所有查看器元件都支援ARIA（可訪問的富網際網路應用程式）角色和屬性，以改進與輔助技術（如螢幕閱讀器）的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video,Accessibility
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有查看器元件都支援ARIA（可訪問的富網際網路應用程式）角色和屬性，以改進與輔助技術（如螢幕閱讀器）的整合。

頂級查看器元素具有角色 `region` 和 `aria-label` 預設設定為查看器名稱的屬性。 可以使用 `Container.LABEL` 本地化符號。

按鈕具有角色 `button` 描述性文本集 `aria-label` 屬性。 值 `aria-label` 屬性是從按鈕的本地化符號的值填充的。 禁用按鈕時， `aria-disabled` 屬性被相應設定。

滑塊元件具有角色 `slider` 使用屬性 `aria-valuenow`。 `aria-valuemin`, `aria-valuemax` 描述當前滑塊位置。

下拉清單由帶有附加項的按鈕激活 `aria-haspopup` 屬性集 `true` 和 `aria-controls` 引用實際下拉面板元素的屬性。 下拉面板本身具有角色 `menu` 具有角色的子元素 `menuitem`。 每個菜單項都 `aria-label` 已指定屬性。

「模式」(Modal)對話框具有角色 `dialog`。 對話框的頭元素由 `aria-labelledby` 屬性。
