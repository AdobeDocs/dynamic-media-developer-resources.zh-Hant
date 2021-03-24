---
description: 事件回呼
solution: Experience Manager
title: 事件回呼
feature: Dynamic Media經典，檢視器，SDK/API,eCatalog搜尋
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---


# 事件回呼{#event-callbacks}

檢視器支援網頁用來追蹤檢視器初始化程式或執行時期行為的JavaScript事件回呼。

回呼處理常式是透過在檢視器的建構函式中，將具有`handlers`屬性的事件名稱和對應處理常式函式傳遞至`config` JSON物件來指派。 或者，也可使用`setHandlers()` API方法。

支援的檢視器事件包括：

* `initComplete` -在檢視器初始化完成並建立所有內部元件時觸發，以便使用 `getComponent()` API。回呼處理常式不會使用任何引數。

* `trackEvent` -在檢視器內每次發生事件時觸發，事件追蹤系統(例如Adobe Analytics)可處理該事件。回呼處理常式會採用下列引數：

   * `objID {String}` 目前未使用。
   * `compClass {String}` 目前未使用。
   * `instName {String}` 觸發事件的檢視器SDK元件的例項名稱。
   * `timeStamp {Number}` 事件時間戳記。
   * `eventInfo {String}` 事件裝載。

另請參閱[eCatalogViewer](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-javascriptapiref/r-html5-ecatsearch-javascriptapiref-ecatalogsearchviewer.md)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856)。
