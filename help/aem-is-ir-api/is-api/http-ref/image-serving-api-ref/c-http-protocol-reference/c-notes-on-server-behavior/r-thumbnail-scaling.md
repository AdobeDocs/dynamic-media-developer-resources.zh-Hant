---
description: 縮圖（即，如果req=tmb）的影像層轉換的步驟2修改如下。
solution: Experience Manager
title: 縮圖縮放
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# 縮圖縮放{#thumbnail-scaling}

縮圖（即，如果req=tmb）的影像層轉換的步驟2修改如下。

* `2.` 如果 `size=` 已指定，請使用縮圖規則讓（已裁切的）影 `size=` 像符合正確。如果未指定`size=`，則根據`res=`縮放，或者，如果未指定`res=`，則使用下面概述的縮圖規則，將（已裁切的）影像調整到畫布中。
