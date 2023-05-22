---
description: 如果請求成功完成，並且請求不包括req=命令，或者req=img或req=tmb，則返回影像資料。
solution: Experience Manager
title: 影像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 1%

---

# 影像{#images}

如果請求成功完成，並且請求不包括req=命令，或者req=img或req=tmb，則返回影像資料。

HTTP響應MIME類型由 `fmt=`，或 `fmt=` 未指定，它 `<image/jpeg>`。

如果請求方法為無條件，則HTTP響應狀態為「200 OK」 `GET` 或 `HEAD`。

伺服器可以以狀態「304」（未修改）答復，並且不返回任何影像資料以響應條件 `GET` 請求(包括有效 `If-Modified-Since` 或 `If-None-Match` 標題)。
