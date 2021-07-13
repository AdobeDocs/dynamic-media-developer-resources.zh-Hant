---
description: 包含與管理影像目錄相關的設定。
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

包含與管理影像目錄相關的設定。

此檔案是JAVA屬性檔案。 必須注意遵循適當的公約；否則，Platform伺服器可能無法啟動。 在Windows檔案路徑中，使用雙反斜線「\\」或單正斜線「/」，而非反斜線「\」。 反斜線在此類型的檔案中用作逸出字元。

此檔案的變更會在檔案儲存後不久生效。

[!DNL catalog-service.conf]中只能更改下列設定。 如果特定設定不存在，則可在檔案中的任何位置新增該設定。 每個設定只能有一個例項。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
