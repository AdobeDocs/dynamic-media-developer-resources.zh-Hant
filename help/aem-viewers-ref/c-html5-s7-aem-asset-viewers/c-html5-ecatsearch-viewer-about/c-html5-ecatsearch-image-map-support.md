---
description: eCatalog搜尋檢視器支援在主檢視上方呈現影像地圖圖示。
solution: Experience Manager
title: 影像地圖支援
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# 影像地圖支援{#image-map-support}

eCatalog搜尋檢視器支援在主檢視上方呈現影像地圖圖示。

如[影像地圖效果](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)中所述，地圖圖示的外觀由CSS控制。

影像映射執行以下三個操作之一：重新導向至外部網頁、「資訊」面板快顯視窗啟動，以及內部超連結。

## 重新導向至外部網頁 {#section-32ebe3c3a7f74892a428c5d48801de4d}

影像映射的`href`屬性具有指向外部資源的URL，可以顯式指定，也可以包裝到支援的JavaScript模板函式之一中：`loadProduct()`、`loadProductCW()`和`loadProductPW()`。

以下是簡單URL重新導向的範例：

`href=http://www.adobe.com`

在此範例中，相同的URL會以`loadProduct()`函式包住：

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

請注意，將JavaScript程式碼新增至影像映射的`HREF`屬性時，該程式碼會在用戶端的電腦上執行。 因此，請確定JavaScript程式碼是安全的。

## 資訊面板彈出式視窗啟動 {#section-7aa036420af646d1ad8cdc388add0b57}

若要使用「資訊」面板，影像映射已設定`ROLLOVER_KEY`屬性。 同時設定`href`屬性，否則外部URL處理會干擾「資訊」面板快顯啟動。

最後，請確定檢視器設定包含`InfoPanelPopup.template`和`InfoPanelPopup.infoServerUrl`參數的適當值（可選）。

>[!NOTE]
>
>請注意，當您設定「資訊面板彈出畫面」時，傳遞至「資訊面板」的HTML程式碼和JavaScript程式碼會在用戶端的電腦上執行。 因此，請確定這類HTML程式碼和JavaScript程式碼是安全的。

## 內部超連結 {#section-6afa4fb2fe564c429e0201f019a95849}

按一下影像地圖會在檢視器內執行內部頁面交換。 若要使用該功能，影像映射中的`href`屬性具有以下特殊格式：

` href=target: *`idx`*`

其中`*`idx`*`是目錄跨頁的零基索引。

以下是指向eCatalog中3D跨頁的影像映射的`href`屬性的示例：

`href=target:2`
