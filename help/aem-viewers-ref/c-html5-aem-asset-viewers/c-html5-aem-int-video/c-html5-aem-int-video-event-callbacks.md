---
description: 事件回呼
solution: Experience Manager
title: 事件回呼
feature: Dynamic Media經典，檢視器，SDK/API，互動式視訊
role: 開發人員，商業從業人員
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '221'
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

* `quickViewActivate` -當使用者在互動式色票元件或視訊播放結束時顯示的「動作呼叫」畫面中點選或點選互動式色票時觸發。回呼處理常式會採用唯一的引數，此引數是具有下列欄位的JSON物件：

   * `sku` {  `String`}與互動式色票關聯的SKU值。
   * `<additionalVariable>` {  `String`}零個或多個與互動色票相關的其他變數。

另請參閱[InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd)和[setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)。
