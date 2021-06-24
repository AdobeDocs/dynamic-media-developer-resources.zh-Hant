---
description: 事件回呼
solution: Experience Manager
title: 事件回呼
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: 21aa4440-c629-440d-b37b-bb98f91ddfd3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# 事件回呼{#event-callbacks}

檢視器支援JavaScript事件回呼，網頁會用來追蹤檢視器初始化程式或執行階段行為。

將具有`handlers`屬性的事件名稱和對應的處理常式函式傳遞至檢視器建構函式中的`config` JSON物件，以指派回呼處理常式。 或者，您也可以使用`setHandlers()` API方法。

支援的檢視器事件包括：

* `initComplete`  — 檢視器初始化完成並建立所有內部元件時觸發，以便能使用 `getComponent()` API。回呼處理常式不採用任何引數。

* `trackEvent`  — 每次在檢視器內發生事件時都會觸發，事件追蹤系統(例如Adobe Analytics)可能會加以處理。回呼處理常式會採用下列引數：

   * `objID {String}` 目前未使用。
   * `compClass {String}` 目前未使用。
   * `instName {String}` 觸發事件的檢視器SDK元件例項名稱。
   * `timeStamp {Number}` 事件時間戳記。
   * `eventInfo {String}` 事件裝載。

另請參閱[eCatalogViewer](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-javascriptapiref/r-html5-ecatsearch-javascriptapiref-ecatalogsearchviewer.md)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856)。
