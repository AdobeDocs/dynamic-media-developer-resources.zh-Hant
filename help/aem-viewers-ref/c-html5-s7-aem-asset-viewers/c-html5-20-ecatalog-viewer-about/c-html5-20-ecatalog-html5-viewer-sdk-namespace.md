---
title: 檢視器SDK名稱空間
description: 檢視器SDK名稱空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: c5286e1f-1f43-4cb8-b876-dc843f8112f5
TQID: 'https://experienceleague.adobe.com/0MMAc-8PpF57-iQSJkEM1n4CjS3z7YWk3boJuiR6bR8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 221
ht-degree: 0%

---

# 檢視器SDK名稱空間{#viewer-sdk-namespace}

檢視器是由許多檢視器SDK元件所建置。 通常網頁不需要直接與SDK元件API互動；所有常見需求都包含在檢視器API本身中。

不過，有些進階使用案例會要求網頁參考使用`getComponent()`檢視器API的內部SDK元件，然後使用SDK本身API的所有彈性。

檢視器用來載入及初始化SDK元件的名稱空間取決於檢視器運作的環境。 如果檢視器在Adobe Experience Manager中執行，檢視器會將SDK元件載入`s7viewers.s7sdk`名稱空間。 而從Dynamic Media Classic提供的檢視器將SDK載入`s7classic.s7sdk`。

在任一情況下，檢視器內SDK使用的名稱空間會以`s7viewers`或`s7classic`作為前置詞。 而且它與SDK使用手冊或SDK API檔案中使用的純`s7sdk`名稱空間不同。

因此，當您編寫與內部檢視器元件通訊的自訂應用程式程式碼時，必須使用完全合格的SDK名稱空間。

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
