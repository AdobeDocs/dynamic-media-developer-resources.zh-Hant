---
description: 所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
solution: Experience Manager
title: 輔助技術支援
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影像，協助工具
role: Developer,Business Practitioner
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色`region`和`aria-label`屬性預設會設為檢視器的名稱。 可以使用`Container.LABEL`本地化符號控制標籤。

主視圖的角色為`application`。 `aria-roledescription`中提供了主視圖的簡要描述，該值由相應主視圖元件的`ROLE_DESCRIPTION`本地化符號定義。 使用`aria-describedby`提供鍵盤用戶的導航提示，使用提示的文本來自`USAGE_HINT`本地化符號。 如果資產在UserData欄位中定義了標籤，則會以該標籤的值設定`aria-label`屬性。

熱點、區域和影像映射具有角色`button`和使用`aria-label`屬性設定的描述性文本，以及熱點或影像映射標籤的值。 當用戶將焦點放在熱點或影像地圖上時，使用`aria-describedby`提供鍵盤用戶的導航提示，使用提示的文本來自`USAGE_HINT`本地化符號。
