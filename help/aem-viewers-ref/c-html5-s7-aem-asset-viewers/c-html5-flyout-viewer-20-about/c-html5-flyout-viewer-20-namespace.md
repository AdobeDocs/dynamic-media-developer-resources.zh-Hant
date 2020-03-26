---
description: 'null'
seo-description: 'null'
seo-title: 檢視器SDK命名空間
solution: Experience Manager
title: 檢視器SDK命名空間
topic: Dynamic media
uuid: 5fa7102b-c93d-4865-9e14-fa8813403de2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 檢視器SDK命名空間{#viewer-sdk-namespace}

檢視器是由許多檢視器SDK元件所建立。 在大多數情況下，網頁不需要直接與SDK元件API互動；檢視器API本身涵蓋所有常見需求。

不過，有些進階使用案例會要求網頁使用檢視器API取得內部SDK元件的參考，然後使用SDK本身API的所有彈性。 `getComponent()`

檢視器用來載入和初始化SDK元件的命名空間取決於檢視器所在的環境。 如果檢視器是在AEM(Adobe Experience Manager)中執行，檢視器會將SDK元件載入命名空間 `s7viewers.s7sdk` 中。 同樣地，從Scene7 Publishing System提供的檢視器會將SDK載入 `s7classic.s7sdk`。

在這兩種情況下，檢視器內的SDK所使用的命名空間會 `s7viewers` 有 `s7classic` 或做為首碼。 此外，它與「SDK使用指南」或「SDK API `s7sdk` 檔案」中使用的簡單名稱空間不同。 因此，當您編寫與內部檢視器元件通訊的自訂應用程式程式碼時，請務必使用完全限定的SDK命名空間。

例如，如果您打算監聽事件，而檢視器是從 `StatusEvent.NOTF_VIEW_READY` AEM提供，則完全限定的事件類型為 `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，而事件接聽程式碼看起來類似下列：

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Scene7 SPS will look like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

