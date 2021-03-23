---
description: 「影像伺服」支援存取外來HTTP和FTP伺服器上的來源影像。
seo-description: 「影像伺服」支援存取外來HTTP和FTP伺服器上的來源影像。
seo-title: 外來影像來源
solution: Experience Manager
title: 外來影像來源
uuid: 28a17400-4807-4e14-937a-80309be53d55
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# 外來影像源{#foreign-image-sources}

「影像伺服」支援存取外來HTTP和FTP伺服器上的來源影像。

為`src=`或`mask=`命令指定外來URL;只需將整個內嵌的URL分隔為大括弧：

` …&src={ *[!DNL foreignUrl]*}&…`

完整絕對URL（若已設定`attribute::AllowDirectUrls`），且允許相對於`attribute::RootUrl`的URL。 如果嵌入了絕對URL且屬性：`AllowDirectUrls`為0，或如果指定了相對URL且`attribute::RootUrl`為空。

伺服器會根據HTTP回應所包含的快取標題，快取外來影像。
