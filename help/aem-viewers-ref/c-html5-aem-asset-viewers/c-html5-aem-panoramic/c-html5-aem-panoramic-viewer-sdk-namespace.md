---
title: 檢視器SDK命名空間
description: 檢視器SDK命名空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3360a3bd-8a4a-4bf9-98bf-ada7c35c58f4
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# 檢視器SDK命名空間{#viewer-sdk-namespace}

檢視器是由許多檢視器SDK元件所建置。 網頁通常不需要直接與SDK元件API互動；檢視器API本身會涵蓋所有常見需求。

不過，部分進階使用案例會要求網頁參考內部SDK元件，使用 `getComponent()` 檢視器API，然後使用SDK本身API的所有彈性。

檢視器用來載入和初始化SDK元件的命名空間取決於檢視器運作的環境。 如果檢視器在Adobe Experience Manager中執行，檢視器會將SDK元件載入至 `s7viewers.s7sdk` 命名空間。 同樣地，Dynamic Media Classic提供的檢視器會將SDK載入至 `s7classic.s7sdk`.

無論是哪種情況，檢視器內的SDK所使用的命名空間皆具有 `s7viewers` 或 `s7classic` 作為首碼。 這和平原不同 `s7sdk` SDK使用手冊或SDK API檔案中使用的命名空間。

因此，撰寫與內部檢視器元件通訊的自訂應用程式程式碼時，請務必使用完全限定的SDK命名空間。

例如，如果您打算 `StatusEvent.NOTF_VIEW_READY` 事件，而檢視器則由Experience Manager提供，則完全限定的事件類型為 `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，而事件接聽程式程式碼看起來類似下列：

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
   panoramicView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
