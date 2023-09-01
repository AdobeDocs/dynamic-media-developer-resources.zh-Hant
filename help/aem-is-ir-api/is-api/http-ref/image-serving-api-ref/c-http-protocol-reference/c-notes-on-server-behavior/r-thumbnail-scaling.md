---
title: 縮圖縮放
description: 影像圖層轉換的步驟2在縮圖上的修改如下（即，如果req=tmb）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# 縮圖縮放{#thumbnail-scaling}

影像圖層轉換的步驟2在縮圖上的修改如下（即，如果req=tmb）。

* `2.` 如果 `size=` 指定，將（裁切的）影像調整到 `size=` 使用縮圖規則矩形。 如果 `size=` 未指定，縮放依據 `res=`，或，如果 `res=` 未指定，請使用下列的縮圖規則將（裁切的）影像調整到畫布矩形。
