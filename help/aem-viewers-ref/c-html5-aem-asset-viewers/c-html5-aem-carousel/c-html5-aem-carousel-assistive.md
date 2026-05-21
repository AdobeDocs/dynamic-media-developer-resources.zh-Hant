---
title: 輔助技術支援
description: 所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
TQID: 'https://experienceleague.adobe.com/GwKu0Nv5i-7DIsa-4JxKiS95NgCpzeoHqb1-LFG8sfg'
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
source-wordcount: 269
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。

最上層檢視器元素具有角色`region`和`aria-label`屬性，預設設定為檢視器的名稱。 您可以使用`Container.LABEL`本地化符號控制標籤。

按鈕具有角色`button`和描述性文字設定了`aria-label`屬性。 `aria-label`屬性的值是從按鈕本地化符號的值填入的。 當按鈕停用時，會相應設定`aria-disabled`屬性。

可讓您瀏覽輪播幻燈片的按鈕具有標籤，這些標籤會根據目前選取的幻燈片在執行階段更新。 這些按鈕標籤的範本設定為`CAROUSELVIEWER_TOOLTIP_GOTO`本地化符號。

主檢視具有角色`application`。 `aria-roledescription`中提供了主檢視的簡短說明，其值是由對應主檢視元件的`ROLE_DESCRIPTION`本地化符號所定義。 使用`aria-describedby`提供鍵盤使用者的導覽提示，使用提示的文字來自`USAGE_HINT`本地化符號。 如果資產在UserData欄位中定義了標籤，則會以此類標籤的值設定`aria-label`屬性。

熱點、區域和影像地圖具有角色`button`和描述性文字集`aria-label`屬性，具有熱點或影像地圖示籤的值。 當使用者將焦點放在熱點或影像地圖上時，會使用`aria-describedby`提供鍵盤使用者的導覽提示，使用提示的文字來自`USAGE_HINT`本地化符號。
