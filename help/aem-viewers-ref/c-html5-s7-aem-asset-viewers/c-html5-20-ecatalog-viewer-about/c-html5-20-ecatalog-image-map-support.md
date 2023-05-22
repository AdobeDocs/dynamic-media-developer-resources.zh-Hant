---
title: 影像映射支援
description: eCatalog查看器支援在主視圖上方呈現影像映射表徵圖。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# 影像映射支援{#image-map-support}

eCatalog查看器支援在主視圖上方呈現影像映射表徵圖。

地圖表徵圖的外觀通過CSS控制，如中所述 [影像映射效果](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)。

影像映射執行以下三個操作之一：重定向至外部網頁、「資訊」面板彈出式激活和內部超連結。

## 重定向至外部網頁 {#section-32ebe3c3a7f74892a428c5d48801de4d}

的 `href` 影像映射的屬性具有指向外部資源的URL，該URL可以顯式指定，也可以包裝到支援的JavaScript模板函式之一中： `loadProduct()`。 `loadProductCW()`, `loadProductPW()`。

以下是簡單URL重定向的示例：

`href=http://www.adobe.com`

在此示例中，同一URL與 `loadProduct()` 函式：

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

將JavaScript代碼添加到 `HREF` 映射的屬性，代碼在客戶端電腦上運行。 因此，請確保JavaScript代碼安全。

## 資訊面板彈出式激活 {#section-7aa036420af646d1ad8cdc388add0b57}

要使用「資訊」面板，影像映射具有 `ROLLOVER_KEY` 屬性集。 另外，設定 `href` 屬性，否則外部URL處理會干擾「資訊」面板彈出式激活。

最後，確保查看器配置包含適當的值 `InfoPanelPopup.template` 和 `InfoPanelPopup.infoServerUrl` 參數。

>[!NOTE]
>
>配置「資訊面板」彈出菜單時，傳遞給「資訊面板」的HTML代碼和JavaScript代碼將在客戶端電腦上運行。 因此，請確保此類HTML代碼和JavaScript代碼是安全的。

## 內部超連結 {#section-6afa4fb2fe564c429e0201f019a95849}

選擇影像映射在查看器內執行內部頁面交換。 要使用該功能， `href` 影像映射中的屬性具有以下特殊格式：

` href=target: *`ID`*`

位置 `*`ID`*` 是目錄擴展的零索引。

以下是 `href` 指向eCatalog中3D跨頁的影像映射的屬性：

`href=target:2`
