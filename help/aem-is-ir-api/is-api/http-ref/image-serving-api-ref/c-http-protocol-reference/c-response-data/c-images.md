---
description: 如果請求成功完成，且請求中未包含req=命令，或req=img或req=tmb，則會傳回影像資料。
solution: Experience Manager
title: 影像
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 1%

---


# 影像{#images}

如果請求成功完成，且請求中未包含req=命令，或req=img或req=tmb，則會傳回影像資料。

HTTP響應MIME類型由`fmt=`確定，或者，如果未指定`fmt=`，則為`<image/jpeg>`。

如果request方法是無條件的`GET`或`HEAD`，則HTTP響應狀態為&#39;200 OK&#39;。

伺服器可以以狀態&#39;304&#39;（未修改）回覆，並且不響應條件式`GET`請求（包括有效的`If-Modified-Since`或`If-None-Match`標題）返回任何影像資料。
