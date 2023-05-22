---
description: 預載入伺服器快取。 執行請求時與req=img類似，但伺服器不返回影像，而是返回回復影像的長度(image.length)，格式化為MIME類型文本/純文字檔案的文本資料。
solution: Experience Manager
title: 載入快取
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# 載入快取{#loadcache}

預載入伺服器快取。 執行請求時與req=img類似，但伺服器不返回影像，而是返回回復影像的長度(image.length)，格式化為MIME類型文本/純文字檔案的文本資料。

`req=loadcache`

HTTP響應不可快取。

請求中的其他命令應用有文檔記錄。
