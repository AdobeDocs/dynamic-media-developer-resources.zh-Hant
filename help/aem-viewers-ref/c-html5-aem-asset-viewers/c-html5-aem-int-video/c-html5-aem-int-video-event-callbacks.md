---
description: 事件回呼
solution: Experience Manager
title: 事件回呼
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '218'
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

* `quickViewActivate`  — 當使用者在互動色票元件內或視訊播放結束時顯示的「呼叫動作」畫面中按一下或點選互動色票時，即觸發此事件。回呼處理常式採用唯一的引數，此引數為具有下列欄位的JSON物件：

   * `sku` {  `String`}與互動式色票關聯的SKU值。
   * `<additionalVariable>` {  `String`}零個或多個與互動式色票相關聯的其他變數。

另請參閱[InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd)和[setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)。
