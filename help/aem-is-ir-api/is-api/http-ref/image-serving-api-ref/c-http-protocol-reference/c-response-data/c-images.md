---
description: 如果請求成功完成，並且請求中未包含req=命令，或者如果req=img或req=tmb，則返回影像資料。
solution: Experience Manager
title: 影像
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---

# 影像{#images}

如果請求成功完成，並且請求中未包含req=命令，或者如果req=img或req=tmb，則返回影像資料。

HTTP響應MIME類型由`fmt=`確定，或者，如果未指定`fmt=`，則為`<image/jpeg>`。

如果要求方法是無條件`GET`或`HEAD`，則HTTP回應狀態為「200 OK」。

伺服器可以以狀態&#39;304&#39;（未修改）回復，並且不返回任何影像資料以響應條件`GET`請求（包括有效的`If-Modified-Since`或`If-None-Match`標頭）。
