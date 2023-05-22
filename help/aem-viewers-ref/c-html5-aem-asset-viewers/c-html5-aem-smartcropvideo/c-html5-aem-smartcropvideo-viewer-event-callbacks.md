---
title: 事件回調
description: 事件回調
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 21962c01-f224-408d-8072-1c7f5d78ac4b
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '154'
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
   * `eventInfo {String}` 事件負載。

另請參閱 [SmartCropVideoViewer]
(/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md和 [setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md)。
