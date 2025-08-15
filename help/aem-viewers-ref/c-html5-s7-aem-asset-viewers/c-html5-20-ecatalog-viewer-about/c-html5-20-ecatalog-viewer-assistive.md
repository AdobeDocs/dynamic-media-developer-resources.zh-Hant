---
title: 輔助技術支援
description: 所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。
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

所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。

最上層檢視器元素具有角色`region`和`aria-label`屬性，預設設定為檢視器的名稱。 您可以使用`Container.LABEL`本地化符號控制標籤。

按鈕具有角色`button`和使用`aria-label`屬性設定的描述性文字。 `aria-label`屬性的值是從按鈕本地化符號的值填入的。 當按鈕停用時，`aria-disabled`屬性會適當地設定。

主檢視具有角色`application`。 `aria-roledescription`中提供了主檢視的簡短說明，其值是由對應主檢視元件的`ROLE_DESCRIPTION`本地化符號所定義。 使用`aria-describedby`提供鍵盤使用者的導覽提示，使用提示的文字來自`USAGE_HINT`本地化符號。 如果資產在UserData欄位中定義了標籤，則會以此類標籤的值設定`aria-label`屬性。

熱點、區域和影像地圖具有角色`button`和描述性文字集`aria-label`屬性，具有熱點或影像地圖示籤的值。 當使用者將焦點放在熱點或影像地圖上時，會使用`aria-describedby`提供鍵盤使用者的導覽提示，使用提示的文字來自`USAGE_HINT`本地化符號。

縮圖具有角色`dialog`，其屬性為`aria-label`，由`ThumbnailGridView.LABEL`本地化符號控制。 個別縮圖具有角色`button`。 如果選取縮圖，它將取得`aria-selected`屬性設定為`true`。

顯示色票的元件具有角色`listbox`，`aria-label`屬性設定為該元件的`LABEL`本地化符號的值。 個別色票具有`option`和`aria-setsize`屬性的角色`aria-posinset`，可說明色票在集中的位置。 如果選取色票，則會將`aria-selected`屬性設定為`true`。

下拉式清單由按鈕啟動，按鈕具有設定為`aria-haspopup`的其他`true`屬性以及參考實際下拉式面板專案的`aria-controls`屬性。 下拉式面板本身具有角色`menu`，其子元素具有角色`menuitem`。 每個功能表專案都指定了`aria-label`屬性。

模型對話方塊具有角色`dialog`。 對話方塊的標頭專案由`aria-labelledby`屬性參考。
