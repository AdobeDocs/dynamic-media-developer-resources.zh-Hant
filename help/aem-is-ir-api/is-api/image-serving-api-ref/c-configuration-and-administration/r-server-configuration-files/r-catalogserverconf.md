---
description: 包含與管理影像目錄相關的設定。
seo-description: 包含與管理影像目錄相關的設定。
seo-title: catalog-server.conf
solution: Experience Manager
title: catalog-server.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 797a43d2-18f5-4735-8b19-da231952b1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# catalog-server.conf{#catalog-server-conf}

包含與管理影像目錄相關的設定。

此檔案是JAVA屬性檔案。 必須注意遵守適當的公約；否則平台伺服器可能無法啟動。 在Windows檔案路徑中，請使用雙反斜線&#39;\\&#39;或單正斜線&#39;/&#39;，而非反斜線&#39;\&#39;。 反斜線用作此類型檔案的轉義字元。

此檔案的變更會在儲存檔案後不久生效。

中只能更改下面列出的設定 [!DNL catalog-service.conf]。 如果某個特定設定不存在，則可以在檔案中的任意位置添加該設定。 每個設定只能有一個例項。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
