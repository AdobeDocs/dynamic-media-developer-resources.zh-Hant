---
description: 在URL或目錄修飾詞命令序列中，圖層定義序列以layer=命令開頭，以另一個layer=命令、effect=命令或URL結尾終止。
seo-description: 在URL或目錄修飾詞命令序列中，圖層定義序列以layer=命令開頭，以另一個layer=命令、effect=命令或URL結尾終止。
seo-title: 指定圖層
solution: Experience Manager
title: 指定圖層
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# 指定圖層{#specifying-layers}

在URL或目錄：:Modifier命令序列中，圖層定義序列以layer=命令開頭，以另一個layer=命令、effect=命令或URL結尾終止。

層定義序列中的所有命令都與層相關聯。

`layer=`命令指定一個層號，該層號必須是整數0或更大。 具有相同圖層編號的圖層定義序列中的所有命令都會套用到相同的圖層。 如果同一命令多次發生，則最後一個實例將佔上風。
