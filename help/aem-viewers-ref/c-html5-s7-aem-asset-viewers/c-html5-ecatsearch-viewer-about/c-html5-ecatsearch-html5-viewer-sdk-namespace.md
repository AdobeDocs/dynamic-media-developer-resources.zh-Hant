---
description: 檢視器SDK名稱空間
solution: Experience Manager
title: 檢視器SDK名稱空間
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 檢視器SDK名稱空間{#viewer-sdk-namespace}

檢視器是由許多檢視器SDK元件所建置。 在大部分的情況下，網頁不需要直接與SDK元件API互動；所有常見需求都在檢視器API本身涵蓋。

不過，有些進階使用案例會要求網頁使用`getComponent()`檢視器API取得內部SDK元件的參考，然後使用SDK本身的API的所有彈性。

檢視器用來載入及初始化SDK元件的名稱空間取決於檢視器運作的環境。 如果檢視器在AEM (Adobe Experience Manager)中執行，檢視器會將SDK元件載入`s7viewers.s7sdk`名稱空間。 而從Dynamic Media Classic提供的檢視器將SDK載入`s7classic.s7sdk`。

在任一情況下，檢視器內SDK使用的名稱空間會以`s7viewers`或`s7classic`作為前置詞。 而且它與SDK使用手冊或SDK API檔案中使用的純`s7sdk`名稱空間不同。

因此，當您編寫與內部檢視器元件通訊的自訂應用程式程式碼時，使用完整限定的SDK名稱空間很重要。

例如，如果您計畫接聽`StatusEvent.NOTF_VIEW_READY`事件，而檢視器是從Dynamic Media Classic提供，則完整事件型別為`s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，而事件接聽程式程式碼類似下列：

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
