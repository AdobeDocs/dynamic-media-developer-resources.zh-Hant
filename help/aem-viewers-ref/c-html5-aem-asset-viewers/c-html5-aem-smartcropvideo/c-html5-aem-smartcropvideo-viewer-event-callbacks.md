---
title: 事件回呼
description: 事件回呼
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: f4db71f503749f086c86353578afe9dc368d04ae
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# 事件回呼{#event-callbacks}

檢視器支援JavaScript事件回呼，網頁會用來追蹤檢視器初始化程式或執行階段行為。

回呼處理常式是透過傳遞事件名稱，以及與 `handlers` 屬性 `config` 檢視器的建構函式中的JSON物件。 或者，可以使用 `setHandlers()` API方法。

支援的檢視器事件包括：

* `initComplete`  — 在檢視器初始化完成並建立所有內部元件時觸發，以便使用 `getComponent()` API。 回呼處理常式不採用任何引數。

* `trackEvent`  — 每次在檢視器內發生事件時都會觸發，事件追蹤系統(例如Adobe Analytics)可能會加以處理。 回呼處理常式會採用下列引數：

   * `objID {String}` 目前未使用。
   * `compClass {String}` 目前未使用。
   * `instName {String}` 觸發事件的檢視器SDK元件例項名稱。
   * `eventInfo {String}` 事件裝載。

另請參閱 [SmartCropVideoViewer]
(/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md)和 [setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md).
