---
description: 「影像伺服」支援存取外來HTTP和FTP伺服器上的來源影像。
seo-description: 「影像伺服」支援存取外來HTTP和FTP伺服器上的來源影像。
seo-title: 外來影像來源
solution: Experience Manager
title: 外來影像來源
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 外來影像來源{#foreign-image-sources}

「影像伺服」支援存取外來HTTP和FTP伺服器上的來源影像。

要指定或命令的 `src=` 外來 `mask=` URL;只需將整個內嵌的URL分隔為大括弧：

` …&src={ *[!DNL foreignUrl]*}&…`

完整絕對URL(如 `attribute::AllowDirectUrls` 果已設定)和相對URL `attribute::RootUrl` 是允許的。 如果嵌入了絕對URL且屬性： `AllowDirectUrls` 為0，或指定相對URL且空 `attribute::RootUrl` 白。

伺服器會根據HTTP回應所包含的快取標題，快取外來影像。
