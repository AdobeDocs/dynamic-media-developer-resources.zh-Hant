---
description: 事件回呼
solution: Experience Manager
title: 事件回呼
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2493208b-9030-49fa-b1fd-2f2bd524bce6
source-git-commit: f4db71f503749f086c86353578afe9dc368d04ae
workflow-type: tm+mt
source-wordcount: '147'
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
   * `timeStamp {Number}` 事件時間戳記。
   * `eventInfo {String}` 事件裝載。

另請參閱 [VideoViewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) 和 [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
