---
description: 「影像伺服」支援在外部HTTP和FTP伺服器上存取來源影像。
solution: Experience Manager
title: 外國影像源
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 外國影像源{#foreign-image-sources}

「影像伺服」支援在外部HTTP和FTP伺服器上存取來源影像。

為`src=`或`mask=`命令指定外來URL;只需以大括弧分隔整個內嵌URL:

` …&src={ *[!DNL foreignUrl]*}&…`

允許完整絕對URL（若已設定`attribute::AllowDirectUrls`）和相對於`attribute::RootUrl`的URL。 如果內嵌絕對URL和屬性，則會發生錯誤：`AllowDirectUrls`為0，或者如果指定了相對URL且`attribute::RootUrl`為空。

伺服器會根據HTTP回應所包含的快取標題，快取外部影像。
