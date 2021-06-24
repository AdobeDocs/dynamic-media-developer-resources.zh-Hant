---
description: 所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。
solution: Experience Manager
title: 輔助技術支援
feature: Dynamic Media Classic，檢視器， SDK/API，縮放，協助工具
role: Developer,Business Practitioner
exl-id: f2f36520-f6dd-4baa-abf0-48a846882acb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA（可存取的豐富網際網路應用程式）角色和屬性，以改善與輔助技術（例如螢幕閱讀器）的整合。

頂層檢視器元素的角色`region`和`aria-label`屬性預設會設為檢視器的名稱。 可以使用`Container.LABEL`本地化符號控制標籤。

按鈕具有角色`button`和使用`aria-label`屬性設定的描述性文本。 從按鈕的本地化符號的值中填入`aria-label`屬性的值。 禁用按鈕時，將相應設定`aria-disabled`屬性。

主視圖的角色為`application`。 `aria-roledescription`中提供了主視圖的簡要描述，該值由相應主視圖元件的`ROLE_DESCRIPTION`本地化符號定義。 使用`aria-describedby`提供鍵盤用戶的導航提示，使用提示的文本來自`USAGE_HINT`本地化符號。 如果資產在UserData欄位中定義了標籤，則會以該標籤的值設定`aria-label`屬性。
