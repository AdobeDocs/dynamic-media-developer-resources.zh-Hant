---
title: Viewer SDK namespace
description: 查看器SDK命名空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: d1f12c9d-9b00-44ee-bd91-76a4d882fecf
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# 查看器SDK命名空間{#viewer-sdk-namespace}

The viewer is built of many Viewer SDK components. Usually, the web page does not need to interact with SDK components API directly; all common needs are covered in the viewer API itself.

但是，某些高級使用情形要求網頁使用 `getComponent()` 查看器API，然後使用SDK本身的API的所有靈活性。

查看器用於載入和初始化SDK元件的命名空間取決於查看器操作的環境。 If the viewer is running in Adobe Experience Manager, the viewer loads SDK components into `s7viewers.s7sdk` namespace. 同樣，從Dynamic Media Classic服務的查看器將SDK載入到 `s7classic.s7sdk`。

在這兩種情況下，查看器內SDK使用的命名空間具有 `s7viewers` 或 `s7classic` 作為前置詞。 它和平原不同 `s7sdk` SDK使用手冊或SDK API文檔中使用的命名空間。 因此，在編寫與內部查看器元件通信的自定義應用程式碼時，必須使用完全限定的SDK命名空間。

例如，如果你打算 `StatusEvent.NOTF_VIEW_READY` 事件和查看器由Experience Manager提供，完全限定的事件類型為 `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，並且事件偵聽器代碼如下所示：

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
