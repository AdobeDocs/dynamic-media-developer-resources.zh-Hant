---
title: 在同一伺服器上安裝多個Dynamic Media檢視器
description: 安裝Dynamic Media檢視器API的指示。
solution: Experience Manager
feature: Dynamic Media Classic，檢視器，SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# 在同一伺服器上安裝多個檢視器{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

安裝Dynamic Media檢視器API的指示。

安裝「影像伺服」檢視器之前，請先安裝並測試「影像伺服」。

將IS Viewers檔案複製到硬碟，然後將`s7viewers.war`檔案部署到`../ImageServing/webapps`目錄。 有關如何部署、啟動、停止和管理映像伺服器的說明，請參閱映像服務文檔。

>[!NOTE]
>
>沒有為Image Serving檢視器安裝升級。 Adobe建議您先備份任何現有的Dynamic Media檢視器(s7viewers)目錄，再繼續安裝。

**要在同一伺服器上安裝多個查看器：**

1. 將檢視器.war重新命名為所需的內容，並將檔案部署至您想要的位置。
1. 在`config.js`中設定`this.isViewerRoot`參數。
1. 開啟位於新建查看器資料夾根目錄的`config.js`。
1. 將參數`this.isViewerRoot = "/s7viewers"`設定為`s7viewers.war`檔案的上下文。 例如，`"/s7viewers-4.0"`。
1. 儲存檔案並關閉。
