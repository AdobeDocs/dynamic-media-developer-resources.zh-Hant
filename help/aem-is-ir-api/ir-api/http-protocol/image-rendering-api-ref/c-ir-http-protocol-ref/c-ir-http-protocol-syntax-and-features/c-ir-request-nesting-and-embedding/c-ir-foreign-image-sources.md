---
title: 外來影像源
description: 映像服務支援訪問外部HTTP和FTP伺服器上的源映像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# 外來影像源{#foreign-image-sources}

映像服務支援訪問外部HTTP和FTP伺服器上的源映像。

指定外來URL `src=` 或 `mask=` 命令；只需用大括弧分隔整個嵌入URL:

` …&src={ *[!DNL foreignUrl]*}&…`

完全絕對URL(如果 `attribute::AllowDirectUrls` 設定)和相對於 `attribute::RootUrl` 的子菜單。 如果嵌入了絕對URL且屬性： `AllowDirectUrls` 為0，或者指定了相對URL並 `attribute::RootUrl` 為空。

伺服器根據HTTP響應所包括的快取頭對外部影像進行快取。
