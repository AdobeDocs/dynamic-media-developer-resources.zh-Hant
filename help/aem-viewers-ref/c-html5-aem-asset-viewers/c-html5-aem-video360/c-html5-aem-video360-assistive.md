---
title: 輔助技術支援
description: 所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video,Accessibility
role: Developer,User
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
TQID: 'https://experienceleague.adobe.com/yODKnwYHQbGZ-BjDs2VwcIiSw3FcGcmuGAgQZmLlzUQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 181
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。

最上層檢視器元素具有角色`region`和`aria-label`屬性，預設設定為檢視器的名稱。 您可以使用`Container.LABEL`本地化符號控制標籤。

按鈕具有角色`button`和描述性文字設定了`aria-label`屬性。 `aria-label`屬性的值是從按鈕本地化符號的值填入的。 當按鈕停用時，會相應設定`aria-disabled`屬性。

Slider元件具有屬性`aria-valuenow`、`aria-valuemin`和`aria-valuemax`的角色`slider`可描述目前的Slider位置。

下拉式清單由按鈕啟動，按鈕具有設定為`true`的其他`aria-haspopup`屬性以及參考實際下拉式面板專案的`aria-controls`屬性。 下拉式面板本身具有角色`menu`，其子元素具有角色`menuitem`。 每個功能表專案都指定了`aria-label`屬性。

模型對話方塊具有角色`dialog`。 對話方塊的標頭專案由`aria-labelledby`屬性參考。
