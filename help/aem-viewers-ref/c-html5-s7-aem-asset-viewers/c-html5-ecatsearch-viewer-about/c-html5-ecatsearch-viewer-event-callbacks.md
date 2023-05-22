---
description: 事件回調
solution: Experience Manager
title: 事件回調
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 21aa4440-c629-440d-b37b-bb98f91ddfd3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '147'
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

另請參閱 [eCatalogViewer](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-javascriptapiref/r-html5-ecatsearch-javascriptapiref-ecatalogsearchviewer.md) 和 [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856)。
