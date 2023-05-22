---
title: 輔助技術支援
description: 所有查看器元件都支援ARIA（可訪問的富網際網路應用程式）角色和屬性，以改進與輔助技術（如螢幕閱讀器）的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有查看器元件都支援ARIA（可訪問的富網際網路應用程式）角色和屬性，以改進與輔助技術（如螢幕閱讀器）的整合。

頂級查看器元素具有角色 `region` 和 `aria-label` 預設設定為查看器名稱的屬性。 可以使用 `Container.LABEL` 本地化符號。

主視圖具有角色 `application`。 中提供了主視圖的簡要說明 `aria-roledescription`，其值由 `ROLE_DESCRIPTION` 相應主視圖元件的本地化符號。 為鍵盤用戶提供導航提示時使用 `aria-describedby`，使用提示的文本來自 `USAGE_HINT` 本地化符號。 如果資產在UserData欄位中定義了標籤， `aria-label` 屬性是使用此類標籤的值設定的。

熱點、區域和影像映射具有作用 `button` 描述性文本集 `aria-label` 屬性，以及熱點或影像映射標籤的值。 當用戶將焦點放在熱點或影像地圖上時，使用 `aria-describedby`，其中使用提示的文本來自 `USAGE_HINT` 本地化符號。
