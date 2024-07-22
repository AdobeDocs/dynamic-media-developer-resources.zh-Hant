---
description: 如果要求成功完成，且要求不包含req=命令或req=img或req=tmb，則會傳回影像資料。
solution: Experience Manager
title: 影像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---

# 影像{#images}

如果要求成功完成，且要求不包含req=命令或req=img或req=tmb，則會傳回影像資料。

HTTP回應MIME型別是由`fmt=`所決定，或者，如果未指定`fmt=`，則是`<image/jpeg>`。

如果要求方法是無條件的`GET`或`HEAD`，則HTTP回應狀態為「200 OK」。

伺服器可能會以狀態&#39;304&#39; （未修改）回覆，且不會傳回任何影像資料以回應條件式`GET`要求（包含有效的`If-Modified-Since`或`If-None-Match`標頭）。
