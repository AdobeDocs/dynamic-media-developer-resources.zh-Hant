---
description: 如果請求成功完成，且請求中未包含req=命令，或req=包含下列值之一，則會傳回影像資料img, debug
seo-description: 如果請求成功完成，且請求中未包含req=命令，或req=包含下列值之一，則會傳回影像資料img, debug
seo-title: 影像
solution: Experience Manager
title: 影像
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---


# 影像{#images}

如果請求成功完成，且請求中未包含req=命令，或req=包含下列值之一，則會傳回影像資料：img, debug

HTTP響應MIME類型由`fmt=`確定，或者，如果未指定`fmt=`，則取決於`attribute::Format`的值。

如果request方法是無條件的`GET`或`HEAD`，則HTTP響應狀態為&#39;200 OK&#39;。

伺服器可以以狀態&#39;304&#39;（未修改）回復，並且不返回任何影像資料以響應條件式`GET`請求（`request-header`中存在[!DNL If-Modified-Since]欄位）。
