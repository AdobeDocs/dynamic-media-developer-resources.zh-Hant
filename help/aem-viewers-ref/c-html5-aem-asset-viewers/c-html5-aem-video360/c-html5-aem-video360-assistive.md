---
description: 所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
solution: Experience Manager
title: 輔助技術支援
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR視訊，協助工具
role: Developer,Business Practitioner
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色`region`和`aria-label`屬性預設會設為檢視器的名稱。 可以使用`Container.LABEL`本地化符號控制標籤。

按鈕具有角色`button`和使用`aria-label`屬性設定的描述性文本。 從按鈕的本地化符號的值中填入`aria-label`屬性的值。 禁用按鈕時，將相應設定`aria-disabled`屬性。

滑桿元件具有`slider`角色，具有`aria-valuenow`、`aria-valuemin`和`aria-valuemax`屬性，以描述當前滑桿位置。

下拉清單由參考實際下拉式面板元素的附加`aria-haspopup`屬性設為`true`和`aria-controls`屬性的按鈕來啟動。 下拉式面板本身具有角色`menu`，其子元素具有角色`menuitem`。 每個菜單項都指定了`aria-label`屬性。

強制回應對話方塊的角色為`dialog`。 `aria-labelledby`屬性引用了對話框的標題元素。
