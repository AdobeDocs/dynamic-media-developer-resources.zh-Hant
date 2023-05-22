---
title: 在同一伺服器上安裝多個Dynamic Media查看器
description: 安裝Dynamic Media查看器API的說明。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# 在同一伺服器上安裝多個查看器{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

安裝Dynamic Media查看器API的說明。

在安裝映像服務查看器之前，請安裝並test映像服務。

將IS查看器檔案複製到硬碟，然後部署 `s7viewers.war` 檔案 `../ImageServing/webapps` 的子菜單。 有關如何部署、啟動、停止和管理映像伺服器的說明，請參閱映像服務文檔。

>[!NOTE]
>
>沒有為映像服務查看器安裝升級。 Adobe建議您先備份任何現有的Dynamic Media查看器(s7viewers)目錄，然後再繼續安裝。

**要在同一伺服器上安裝多個查看器：**

1. 將查看器.war更名為所需上下文，並將檔案部署到所需位置。
1. 設定 `this.isViewerRoot` 參數 `config.js`。
1. 開啟 `config.js` 位於新建立的查看器資料夾的根目錄。
1. 設定參數 `this.isViewerRoot = "/s7viewers"` 到 `s7viewers.war` 的子菜單。 例如，`"/s7viewers-4.0"`。
1. 保存檔案並關閉。
