---
description: 對縮略圖（即，如果req=tmb），如下修改影像層轉換的步驟2。
solution: Experience Manager
title: 縮略圖縮放
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# 縮略圖縮放{#thumbnail-scaling}

對縮略圖（即，如果req=tmb），如下修改影像層轉換的步驟2。

* `2.` 如果 `size=` 指定，將（裁剪的）影像調整到 `size=` 使用縮略圖規則直接。 如果 `size=` 未指定，基於 `res=`，或 `res=` 未指定，請使用下面概述的縮略圖規則將（裁剪的）影像調整到畫布中。
