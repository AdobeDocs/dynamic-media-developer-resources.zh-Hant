---
description: eCatalog Search Viewer支援在主檢視上方呈現影像地圖圖示。
seo-description: eCatalog Search Viewer支援在主檢視上方呈現影像地圖圖示。
seo-title: 影像地圖支援
solution: Experience Manager
title: 影像地圖支援
topic: Dynamic media
uuid: 22ba8168-b384-4eda-a147-ce8172cfed11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 影像地圖支援{#image-map-support}

eCatalog Search Viewer支援在主檢視上方呈現影像地圖圖示。

地圖圖示的外觀由CSS控制，如影像地圖 [效果所述](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)。

影像地圖會執行下列三個動作之一：重新導向至外部網頁、「資訊」面板快顯啟動和內部超連結。

## 重新導向至外部網頁 {#section-32ebe3c3a7f74892a428c5d48801de4d}

影 `href` 像映射的屬性具有外部資源的URL，可明確指定，或封裝在支援的JavaScript範本函式中： `loadProduct()`、 `loadProductCW()`和 `loadProductPW()`。

以下是簡單URL重新導向的範例：

`href=http://www.adobe.com`

在此範例中，相同的URL會與函式包 `loadProduct()` 住：

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Be aware that when you add the JavaScript code into the `HREF` attribute of your image map, the code is run on the client’s computer. 因此，請確定JavaScript程式碼是安全的。

## 資訊面板快顯啟動 {#section-7aa036420af646d1ad8cdc388add0b57}

若要使用「資訊」面板，影像地圖會設定 `ROLLOVER_KEY` 屬性。 此外，同時 `href` 設定屬性，否則外部URL處理會干擾「資訊」面板快顯啟動。

最後，請確定檢視器組態包含適當的參數 `InfoPanelPopup.template` 值，以及（可選） `InfoPanelPopup.infoServerUrl` 參數。

>[!NOTE]
>
>請注意，當您設定「資訊面板彈出畫面」時，傳送至「資訊面板」的HTML程式碼和JavaScript程式碼會在用戶端的電腦上執行。 因此，請確定此類HTML程式碼和JavaScript程式碼是安全的。

## 內部超連結 {#section-6afa4fb2fe564c429e0201f019a95849}

按一下影像地圖會在檢視器內執行內部頁面交換。 若要使用該功能，影 `href` 像地圖中的屬性會有下列特殊格式：

` href=target: *`idx`*`

其 ` *`中`*` idx是目錄跨頁的零索引。

以下是指向eCatalog中 `href` 3D跨頁的影像地圖屬性範例：

`href=target:2`
