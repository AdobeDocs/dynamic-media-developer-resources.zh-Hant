---
description: 檢視器SDK命名空間
solution: Experience Manager
title: 檢視器SDK命名空間
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---


# 檢視器SDK命名空間{#viewer-sdk-namespace}

檢視器是由許多檢視器SDK元件所建立。 在大多數情況下，網頁不需要直接與SDK元件API互動；檢視器API本身涵蓋所有常見需求。

不過，有些進階使用案例會要求網頁使用`getComponent()`檢視器API取得內部SDK元件的參考，然後使用SDK本身API的所有彈性。

檢視器用來載入和初始化SDK元件的命名空間取決於檢視器所在的環境。 如果檢視器在(Adobe Experience Manager)AEM中執行，檢視器會將SDK元件載入至`s7viewers.s7sdk`命名空間。 而且，從Dynamic MediaClassic提供的檢視器會將SDK載入`s7classic.s7sdk`。

無論何種情況，檢視器內的SDK所使用的命名空間會以`s7viewers`或`s7classic`為首碼。 此外，它與「SDK使用指南」或SDK API檔案中使用的簡單`s7sdk`命名空間不同。

因此，當您編寫與內部檢視器元件通訊的自訂應用程式程式碼時，請務必使用完全限定的SDK命名空間。

例如，如果您打算監聽`StatusEvent.NOTF_VIEW_READY`事件，而檢視器是從Dynamic Media經典網站提供，則完全限定的事件類型為`s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，而事件監聽器程式碼看起來類似下列：

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

