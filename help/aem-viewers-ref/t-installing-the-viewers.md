---
title: 在同一部伺服器上安裝多個Dynamic Media檢視器
description: Dynamic Media檢視器API的安裝指示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
TQID: 'https://experienceleague.adobe.com/Zz0BTc333AIELPKRWFeIxhNvTyOJZH1RHLYNvZpt-ZY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 1%

---

# 在同一部伺服器上安裝多個檢視器{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Dynamic Media檢視器API的安裝指示。

安裝「影像伺服」檢視器之前，請先安裝並測試「影像伺服」。

將IS Viewers檔案複製到硬碟，然後將`s7viewers.war`檔案部署到`../ImageServing/webapps`目錄。 如需如何部署、啟動、停止及管理影像伺服器的指示，請參閱您的影像伺服檔案。

>[!NOTE]
>
>「影像伺服」檢視器沒有升級安裝。 Adobe建議您先備份任何現有的Dynamic Media檢視器(s7viewers)目錄，再繼續安裝。

**若要在同一伺服器上安裝多個檢視器：**

1. 將檢視器.war重新命名為所要的前後關聯，並將檔案部署至所要的位置。
1. 在`config.js`中設定`this.isViewerRoot`引數。
1. 在新建立的檢視器資料夾的根目錄中開啟`config.js`。
1. 將引數`this.isViewerRoot = "/s7viewers"`設定為`s7viewers.war`檔案的內容。 例如，`"/s7viewers-4.0"`。
1. 儲存檔案並關閉。
