---
description: 對縮圖（即，如果req=tmb）的影像層變換的步驟2進行如下修改。
seo-description: 對縮圖（即，如果req=tmb）的影像層變換的步驟2進行如下修改。
seo-title: 縮圖縮放
solution: Experience Manager
title: 縮圖縮放
topic: Scene7 Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# 縮圖縮放{#thumbnail-scaling}

對縮圖（即，如果req=tmb）的影像層變換的步驟2進行如下修改。

* `2.` 如果 `size=` 已指定，請使用縮圖規則將（裁切的）影像 `size=` 調整為正確。如果未指定`size=`，則根據`res=`縮放，或者，如果未指定`res=`，則使用下列縮圖規則將（裁切的）影像調整到畫布中。

