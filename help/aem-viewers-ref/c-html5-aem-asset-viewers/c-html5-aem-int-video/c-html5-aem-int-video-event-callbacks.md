---
title: 事件回調
description: 事件回調
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# 事件回調{#event-callbacks}

查看器支援JavaScript事件回調，該Web頁用於跟蹤查看器初始化進程或運行時行為。

通過傳遞事件名稱和相應的處理程式函式 `handlers` 屬性 `config` 查看器的建構子中的JSON對象。 或者，可以使用 `setHandlers()` API方法。

支援的查看器事件包括：

* `initComplete`  — 在完成查看器初始化並建立所有內部元件時觸發，以便 `getComponent()` API。 回調處理程式不採用任何參數。
* `trackEvent`  — 每次在查看器內發生事件時觸發，事件跟蹤系統可以處理這些事件，如Adobe Analytics。 回調處理程式採用以下參數：

   * `objID {String}` 當前未使用。
   * `compClass {String}` 當前未使用。
   * `instName {String}` 觸發事件的Viewer SDK元件的實例名稱。
   * `timeStamp {Number}` 事件時間戳。
   * `eventInfo {String}` 事件負載。

* `quickViewActivate`  — 當用戶按一下或點擊互動式色板元件或視頻播放結束時顯示的「操作呼叫」螢幕中的互動式色板時觸發。 回調處理程式只使用JSON對象的參數，其中包含以下欄位：

   * `sku` { 0} `String`}與交互色板關聯的SKU值。
   * `<additionalVariable>` { 0} `String`}零個或多個與交互色板關聯的附加變數。

另請參閱 [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) 和 [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)。
