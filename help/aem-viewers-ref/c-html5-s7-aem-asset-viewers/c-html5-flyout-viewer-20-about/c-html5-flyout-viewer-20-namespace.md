---
title: 檢視器SDK名稱空間
description: 檢視器SDK名稱空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 06a7110a-3a6f-42f9-b729-e8f96762c64e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# 檢視器SDK名稱空間{#viewer-sdk-namespace}

檢視器是由許多Viewer SDK元件所建置。 通常網頁不需要直接與SDK元件API互動；所有常見需求都包含在檢視器API本身中。

不過，有些進階使用案例會要求網頁參考使用`getComponent()`檢視器API的內部SDK元件，然後使用SDK本身的API的所有彈性。

檢視器用來載入及初始化SDK元件的名稱空間取決於檢視器運作的環境。 如果檢視器在Adobe Experience Manager中執行，檢視器會將SDK元件載入`s7viewers.s7sdk`名稱空間。 同樣地，Dynamic Media Classic提供的檢視器會將SDK載入`s7classic.s7sdk`。

無論是哪種情況，檢視器內SDK使用的名稱空間會以`s7viewers`或`s7classic`作為前置詞。 此外，它與SDK使用手冊或SDK API檔案中使用的純`s7sdk`名稱空間不同。 因此，撰寫可與內部檢視器元件通訊的自訂應用程式程式碼時，必須使用完整限定的SDK名稱空間。

例如，如果您計畫接聽`StatusEvent.NOTF_VIEW_READY`事件，而檢視器是從Experience Manager提供，則完整事件型別為`s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，而事件接聽程式程式碼看起來類似下列：

```html {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic looks like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
