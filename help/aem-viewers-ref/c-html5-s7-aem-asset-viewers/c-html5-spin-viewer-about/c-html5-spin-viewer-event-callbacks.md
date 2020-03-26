---
description: 'null'
seo-description: 'null'
seo-title: 事件回呼
solution: Experience Manager
title: 事件回呼
topic: Dynamic media
uuid: 512f5c08-cf6a-4721-a169-11977cd4c248
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

另請參 [閱SpinViewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195) 和 [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef)。
