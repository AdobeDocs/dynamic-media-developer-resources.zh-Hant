---
title: 在同一台伺服器上安裝多個Dynamic Media查看器
description: 安裝Dynamic Media檢視器API的指示。
solution: Experience Manager
feature: Dynamic Media經典，檢視器，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# 在同一台伺服器上安裝多個查看器{#installing-multiple-viewers-on-the-same-server}

<!-- Updated January 13, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

安裝Dynamic Media檢視器API的指示。

安裝影像伺服檢視器前，請先安裝並測試影像伺服。

將IS查看器檔案複製到硬碟，然後將`s7viewers.war`檔案部署到`../ImageServing/webapps`目錄。 如需如何部署、啟動、停止和管理影像伺服器的指示，請參閱影像伺服檔案。

>[!NOTE]
>
>Image Serving檢視器不需安裝升級版。 Adobe建議您先備份任何現有的Dynamic Media檢視器(s7viewers)目錄，然後再繼續安裝。

**若要在同一伺服器上安裝多個檢視器**

1. 將檢視器。war重新命名為所要的內容，並將檔案部署至您想要的位置。
1. 在`config.js`中設定`this.isViewerRoot`參數。
1. 開啟位於新建立之檢視器資料夾根目錄的`config.js`。
1. 將參數`this.isViewerRoot = "/s7viewers"`設定為`s7viewers.war`檔案的上下文。 例如，`"/s7viewers-4.0"`。
1. 儲存檔案並關閉。
