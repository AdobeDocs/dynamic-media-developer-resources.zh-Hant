---
description: 包含與管理映像目錄相關的設定。
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

包含與管理映像目錄相關的設定。

此檔案是JAVA屬性檔案。 必須注意遵守適當的公約；否則 [!DNL Platform Server] 可能無法啟動。 在Windows檔案路徑中，使用雙反斜線「\\」或單正斜線「/」，而不是反斜線「\」。 反斜線用作此類檔案中的轉義字元。

對此檔案所做的更改將在檔案保存後不久生效。

只能在中更改下面列出的設定 [!DNL catalog-service.conf]。 如果缺少特定設定，則可以在檔案的任何位置添加該設定。 每個設定只能有一個實例。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
