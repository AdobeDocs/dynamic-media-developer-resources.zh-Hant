---
title: 影像地圖支援
description: eCatalog檢視器支援在主檢視上方呈現影像地圖圖示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 影像地圖支援{#image-map-support}

eCatalog檢視器支援在主檢視上方呈現影像地圖圖示。

地圖圖示的外觀是透過CSS控制，如 [影像地圖效果](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

影像映射執行以下三個操作之一：重新導向至外部網頁、「資訊」面板快顯視窗啟動，以及內部超連結。

## 重新導向至外部網頁 {#section-32ebe3c3a7f74892a428c5d48801de4d}

此 `href` 影像映射的屬性具有外部資源的URL，可明確指定或包裝到支援的JavaScript範本函式之一中： `loadProduct()`, `loadProductCW()`，和 `loadProductPW()`.

以下是簡單URL重新導向的範例：

`href=http://www.adobe.com`

在此範例中，相同的URL會以 `loadProduct()` 函式：

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

將JavaScript程式碼新增至 `HREF` 屬性，則程式碼會在用戶端的電腦上執行。 因此，請確定JavaScript程式碼是安全的。

## 資訊面板彈出式視窗啟動 {#section-7aa036420af646d1ad8cdc388add0b57}

若要使用「資訊」面板，影像地圖會使用 `ROLLOVER_KEY` 屬性集。 此外，設定 `href` 屬性，否則外部URL處理會干擾「資訊」面板快顯啟動。

最後，請確定檢視器設定包含 `InfoPanelPopup.template` 和（可選） `InfoPanelPopup.infoServerUrl` 參數。

>[!NOTE]
>
>當您設定「資訊面板彈出畫面」時，傳遞至「資訊面板」的HTML代碼和JavaScript代碼會在用戶端的電腦上執行。 因此，請確定這類HTML程式碼和JavaScript程式碼是安全的。

## 內部超連結 {#section-6afa4fb2fe564c429e0201f019a95849}

選取影像地圖會在檢視器內執行內部頁面交換。 若要使用該功能，請 `href` 屬性的下列特殊格式：

` href=target: *`idx`*`

其中 `*`idx`*` 是目錄擴散的零基索引。

以下是 `href` 屬性，該屬性指向eCatalog中的3D跨頁：

`href=target:2`
