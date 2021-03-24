---
description: 「影像伺服」支援存取外來HTTP和FTP伺服器上的來源影像。
solution: Experience Manager
title: 外來影像來源
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# 外來影像源{#foreign-image-sources}

「影像伺服」支援存取外來HTTP和FTP伺服器上的來源影像。

為`src=`或`mask=`命令指定外來URL;只需將整個內嵌的URL分隔為大括弧：

` …&src={ *[!DNL foreignUrl]*}&…`

完整絕對URL（若已設定`attribute::AllowDirectUrls`），且允許相對於`attribute::RootUrl`的URL。 如果嵌入了絕對URL且屬性：`AllowDirectUrls`為0，或如果指定了相對URL且`attribute::RootUrl`為空。

伺服器會根據HTTP回應所包含的快取標題，快取外來影像。
