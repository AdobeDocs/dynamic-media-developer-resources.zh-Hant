---
title: 事件回呼
description: 事件回呼
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2493208b-9030-49fa-b1fd-2f2bd524bce6
TQID: 'https://experienceleague.adobe.com/-P5-isdXSmYHGdRQ6Ao1hUvsqfuHRG0xgkoe2Qr9mG8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 0%

---

# 事件回呼{#event-callbacks}

檢視器支援網頁用來追蹤檢視器初始化程式或執行階段行為的JavaScript事件回呼。

將事件名稱和對應的處理常式函式（具有`handlers`屬性）傳遞給檢視器建構函式中的`config` JSON物件，即可指派回呼處理常式。 或者，也可以使用`setHandlers()` API方法。

支援的檢視器事件包括：

* `initComplete` — 當檢視器初始化完成並建立所有內部元件時觸發，以便可以使用`getComponent()` API。 回呼處理常式不接受任何引數。

* `trackEvent` — 每次在檢視器內發生事件時都會觸發，該事件可能由事件追蹤系統（例如Adobe Analytics）處理。 回呼處理常式會採用下列引數：

   * `objID {String}`目前未使用。
   * `compClass {String}`目前未使用。
   * `instName {String}`觸發事件的檢視器SDK元件的執行個體名稱。
   * `timeStamp {Number}`事件時間戳記。
   * `eventInfo {String}`個事件承載。

另請參閱[VideoViewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926)。
