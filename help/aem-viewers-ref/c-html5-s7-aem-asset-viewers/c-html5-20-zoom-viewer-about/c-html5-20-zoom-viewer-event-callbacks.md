---
title: 事件回呼
description: 事件回呼
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 68aa55da-5f6f-4c7d-8d3f-c25de9cc325c
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# 事件回呼{#event-callbacks}

檢視器支援網頁用來追蹤檢視器初始化程式或執行階段行為的JavaScript事件回呼。

將事件名稱和對應的處理常式函式（具有`handlers`屬性）傳遞給檢視器建構函式中的`config` JSON物件，即可指派回呼處理常式。 或者，也可以使用`setHandlers()` API方法。

支援的檢視器事件包括：

* `initComplete` — 當檢視器初始化完成並建立所有內部元件時觸發，以便可以使用`getComponent()` API。 回呼處理常式不接受任何引數。

* `trackEvent` — 每次在檢視器內發生事件時都會觸發，該事件可能由事件追蹤系統(例如Adobe Analytics)處理。 回呼處理常式會採用下列引數：

   * `objID {String}`目前未使用。
   * `compClass {String}`目前未使用。
   * `instName {String}`觸發事件的檢視器SDK元件的執行個體名稱。
   * `timeStamp {Number}`事件時間戳記。
   * `eventInfo {String}`個事件承載

另請參閱[ZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-zoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)。
