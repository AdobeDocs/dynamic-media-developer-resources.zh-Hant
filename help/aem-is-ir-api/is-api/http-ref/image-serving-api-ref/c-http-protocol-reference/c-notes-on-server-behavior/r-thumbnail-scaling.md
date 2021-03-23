---
description: 對縮圖（即，如果req=tmb）的影像層變換的步驟2進行如下修改。
seo-description: 對縮圖（即，如果req=tmb）的影像層變換的步驟2進行如下修改。
seo-title: 縮圖縮放
solution: Experience Manager
title: 縮圖縮放
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# 縮圖縮放{#thumbnail-scaling}

對縮圖（即，如果req=tmb）的影像層變換的步驟2進行如下修改。

* `2.` 如果 `size=` 已指定，請使用縮圖規則將（裁切的）影像 `size=` 調整為正確。如果未指定`size=`，則根據`res=`縮放，或者，如果未指定`res=`，則使用下列縮圖規則將（裁切的）影像調整到畫布中。

