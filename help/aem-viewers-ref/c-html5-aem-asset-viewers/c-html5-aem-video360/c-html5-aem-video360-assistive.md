---
title: 輔助技術支援
description: 所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video,Accessibility
role: Developer,User
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。

最上層檢視器元素具有角色`region`和`aria-label`屬性，預設設定為檢視器的名稱。 您可以使用`Container.LABEL`本地化符號控制標籤。

按鈕具有角色`button`和描述性文字設定了`aria-label`屬性。 `aria-label`屬性的值是從按鈕本地化符號的值填入的。 當按鈕停用時，會相應設定`aria-disabled`屬性。

Slider元件具有屬性`slider`、`aria-valuenow`和`aria-valuemin`的角色`aria-valuemax`可描述目前的Slider位置。

下拉式清單由按鈕啟動，按鈕具有設定為`aria-haspopup`的其他`true`屬性以及參考實際下拉式面板專案的`aria-controls`屬性。 下拉式面板本身具有角色`menu`，其子元素具有角色`menuitem`。 每個功能表專案都指定了`aria-label`屬性。

模型對話方塊具有角色`dialog`。 對話方塊的標頭專案由`aria-labelledby`屬性參考。
