---
description: 如果請求成功完成，且請求中未包含req=命令，或req=img或req=tmb，則會傳回影像資料。
seo-description: 如果請求成功完成，且請求中未包含req=命令，或req=img或req=tmb，則會傳回影像資料。
seo-title: 影像
solution: Experience Manager
title: 影像
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# 影像{#images}

如果請求成功完成，且請求中未包含req=命令，或req=img或req=tmb，則會傳回影像資料。

HTTP響應MIME類型由`fmt=`確定，或者，如果未指定`fmt=`，則為`<image/jpeg>`。

如果request方法是無條件的`GET`或`HEAD`，則HTTP響應狀態為&#39;200 OK&#39;。

伺服器可以以狀態&#39;304&#39;（未修改）回覆，並且不響應條件式`GET`請求（包括有效的`If-Modified-Since`或`If-None-Match`標題）返回任何影像資料。
