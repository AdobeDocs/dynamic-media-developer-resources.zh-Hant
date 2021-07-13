---
description: 檢視器SDK命名空間
solution: Experience Manager
title: 檢視器SDK命名空間
feature: Dynamic Media Classic，檢視器，SDK/API，回轉集
role: Developer,User
exl-id: 2b4b0b31-3c88-42a4-8a81-5534691e318f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 檢視器SDK命名空間{#viewer-sdk-namespace}

檢視器是由許多檢視器SDK元件所建置。 在大多數情況下，網頁不需要直接與SDK元件API互動；檢視器API本身會涵蓋所有常見需求。

不過，有些進階使用案例會要求網頁使用`getComponent()`檢視器API來取得內部SDK元件的參考，然後使用SDK本身API的所有彈性。

檢視器用來載入和初始化SDK元件的命名空間取決於檢視器運作的環境。 如果檢視器在AEM(Adobe Experience Manager)中執行，檢視器會將SDK元件載入至`s7viewers.s7sdk`命名空間。 同樣地，Dynamic Media Classic提供的檢視器會將SDK載入`s7classic.s7sdk`中。

無論是哪種情況，檢視器內的SDK所使用的命名空間會以`s7viewers`或`s7classic`作為首碼。 此外，它與SDK使用指南或SDK API檔案中使用的純`s7sdk`命名空間不同。 因此，撰寫與內部檢視器元件通訊的自訂應用程式程式碼時，請務必使用完全限定的SDK命名空間。

例如，如果您打算監聽`StatusEvent.NOTF_VIEW_READY`事件，且檢視器是從AEM提供，則完全限定的事件類型為`s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，而事件監聽器程式碼看起來類似於下列：

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var spinView = <instance>.getComponent("spinView"); 
   spinView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var spinView = <instance>.getComponent("spinView"); 
   spinView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
