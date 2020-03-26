---
description: 安裝Scene7檢視器API的指示。
seo-description: 安裝Scene7檢視器API的指示。
seo-title: 在同一台伺服器上安裝多個查看器
solution: Experience Manager
title: 在同一台伺服器上安裝多個查看器
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 在同一台伺服器上安裝多個查看器{#installing-multiple-viewers-on-the-same-server}

安裝Scene7檢視器API的指示。

安裝影像伺服檢視器前，請先安裝並測試影像伺服。

將IS檢視器檔案複製到硬碟，然後將檔 `s7viewers.war` 案部署至目 `../ImageServing/webapps` 錄。 如需如何部署、啟動、停止和管理影像伺服器的指示，請參閱影像伺服檔案。

>[!NOTE]
>
>Image Serving檢視器不需安裝升級版。 Adobe建議您先備份任何現有的Scene7檢視器目錄，然後再繼續安裝。

**若要將檢視器安裝在同一伺服器上**

1. 將檢視器。war重新命名為所要的內容，並將檔案部署至您想要的位置。
1. 在中 `this.isViewerRoot` 設定參 `config.js`數。
1. 開啟 `config.js` 位於新建檢視器資料夾根目錄中。
1. 將參數 `this.isViewerRoot = "/s7viewers"` 設定為檔案的上 `s7viewers.war` 下文。 例如, `"/s7viewers-4.0"`. 儲存並關閉檔案。
1. 儲存檔案並關閉。
