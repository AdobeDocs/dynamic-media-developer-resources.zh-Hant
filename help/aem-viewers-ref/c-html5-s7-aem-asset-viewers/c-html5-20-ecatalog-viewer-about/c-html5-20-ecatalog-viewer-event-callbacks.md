---
description: 'null'
seo-description: 'null'
seo-title: 事件回呼
solution: Experience Manager
title: 事件回呼
topic: Dynamic media
uuid: 8afb5a98-45f2-4319-bece-70c27f0f68dc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 事件回呼{#event-callbacks}

檢視器支援網頁用來追蹤檢視器初始化程式或執行時期行為的JavaScript事件回呼。

回呼處理常式是透過在檢視器的建構函式中，將事件名稱和具有屬性的 `handlers` 對應處理常式函 `config` 數傳遞至JSON物件來指派。 或者，也可以使用 `setHandlers()` API方法。

支援的檢視器事件包括：

* `initComplete` -在檢視器初始化完成並建立所有內部元件時觸發，以便使用 `getComponent()` API。 回呼處理常式不會使用任何引數。

* `trackEvent` -每次在檢視器內發生事件時觸發，事件追蹤系統（例如Adobe Analytics）可能會處理該事件。 回呼處理常式會採用下列引數：

   * `objID {String}` 目前未使用。
   * `compClass {String}` 目前未使用。
   * `instName {String}` 觸發事件的檢視器SDK元件的例項名稱。
   * `timeStamp {Number}` 事件時間戳記。
   * `eventInfo {String}` 事件裝載。

另請參 [閱eCatalogViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-ecatalogviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) 和 [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856)。
