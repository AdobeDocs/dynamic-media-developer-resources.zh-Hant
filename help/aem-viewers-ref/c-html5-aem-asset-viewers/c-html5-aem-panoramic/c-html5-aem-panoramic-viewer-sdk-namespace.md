---
title: 檢視器SDK名稱空間
description: 檢視器SDK名稱空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3360a3bd-8a4a-4bf9-98bf-ada7c35c58f4
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# 檢視器SDK名稱空間{#viewer-sdk-namespace}

檢視器是由許多Viewer SDK元件所建置。 通常網頁不需要直接與SDK元件API互動；所有常見需求都包含在檢視器API本身中。

不過，有些進階使用案例會要求網頁參考使用中的內部SDK元件 `getComponent()` 檢視器API，然後運用SDK本身API的所有彈性。

檢視器用來載入及初始化SDK元件的名稱空間取決於檢視器運作的環境。 如果檢視器在Adobe Experience Manager中執行，檢視器會將SDK元件載入到 `s7viewers.s7sdk` 名稱空間。 同樣地，Dynamic Media Classic提供的檢視器會將SDK載入 `s7classic.s7sdk`.

無論是哪種情況，檢視器內SDK使用的名稱空間都會 `s7viewers` 或 `s7classic` 做為前置詞。 而且，它和一般情況不同 `s7sdk` SDK使用手冊或SDK API檔案中使用的名稱空間。

因此，撰寫可與內部檢視器元件通訊的自訂應用程式程式碼時，必須使用完整限定的SDK名稱空間。

例如，如果您計畫接聽 `StatusEvent.NOTF_VIEW_READY` 事件且檢視器是從Experience Manager提供，則完整的事件型別為 `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，則事件接聽程式程式碼會如下所示：

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
   panoramicView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
