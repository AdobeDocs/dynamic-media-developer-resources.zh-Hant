---
description: 對縮圖（即，如果req=tmb）的影像層變換的步驟2進行如下修改。
solution: Experience Manager
title: 縮圖縮放
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# 縮圖縮放{#thumbnail-scaling}

對縮圖（即，如果req=tmb）的影像層變換的步驟2進行如下修改。

* `2.` 如果 `size=` 已指定，請使用縮圖規則將（裁切的）影像 `size=` 調整為正確。如果未指定`size=`，則根據`res=`縮放，或者，如果未指定`res=`，則使用下列縮圖規則將（裁切的）影像調整到畫布中。

