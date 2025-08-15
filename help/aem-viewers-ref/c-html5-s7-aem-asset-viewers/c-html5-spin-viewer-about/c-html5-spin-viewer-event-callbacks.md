---
title: 事件回呼
description: 事件回呼
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 26f1dd99-fee9-4a71-9ec1-cfd1e29cb886
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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
   * `eventInfo {String}`個事件承載。

另請參閱[SpinViewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef)。
