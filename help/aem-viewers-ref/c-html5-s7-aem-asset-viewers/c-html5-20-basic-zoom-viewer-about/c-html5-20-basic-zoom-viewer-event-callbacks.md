---
title: 事件回呼
description: 事件回呼
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 14b317ab-82fb-4f55-babe-72c24e6afc2c
source-git-commit: d5f1f05c36c1cb8a57b5a4bb8a9d066c20e32e75
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
   * `instName {String}`觸發事件之Viewer SDK元件的執行個體名稱。
   * `timeStamp {Number}`事件時間戳記。
   * `eventInfo {String}`個事件承載。

另請參閱[BasicZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-basiczoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-b748b29eaafa463a9d1723cb7b86f0d9)。
