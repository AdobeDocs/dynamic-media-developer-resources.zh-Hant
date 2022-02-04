---
title: 查看器SDK命名空間
description: 查看器SDK命名空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 570f8eee-a7dd-40aa-b732-03f97d2544c0
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# 查看器SDK命名空間{#viewer-sdk-namespace}

查看器由許多查看器SDK元件構建。 通常，網頁不需要直接與SDK元件API交互；查看器API本身涵蓋所有常見需求。

但是，某些高級使用情形要求網頁使用 `getComponent()` 查看器API，然後使用SDK本身的API的所有靈活性。

查看器用於載入和初始化SDK元件的命名空間取決於查看器操作的環境。 如果查看器在Adobe Experience Manager運行，則查看器將SDK元件載入到 `s7viewers.s7sdk` 命名空間。 同樣，從Dynamic Media Classic服務的查看器將SDK載入到 `s7classic.s7sdk`。

在這兩種情況下，查看器內SDK使用的命名空間具有 `s7viewers` 或 `s7classic` 作為前置詞。 它和平原不同 `s7sdk` SDK使用手冊或SDK API文檔中使用的命名空間。 因此，在編寫與內部查看器元件通信的自定義應用程式碼時，必須使用完全限定的SDK命名空間。

例如，如果你打算 `StatusEvent.NOTF_VIEW_READY` 事件和查看器由Experience Manager提供，完全限定的事件類型為 `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，並且事件偵聽器代碼如下所示：

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
