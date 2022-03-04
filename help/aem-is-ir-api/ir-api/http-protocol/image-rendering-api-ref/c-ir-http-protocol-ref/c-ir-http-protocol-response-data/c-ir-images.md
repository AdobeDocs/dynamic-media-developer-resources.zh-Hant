---
title: 影像
description: 如果請求成功完成，並且請求中不包含req=命令，或者req=具有以下值之一img, debug，則返回影像資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---

# 影像{#images}

如果請求成功完成，並且請求中不包含req=命令，或者req=具有以下值之一，則返回影像資料：img，調試

HTTP響應MIME類型由 `fmt=`，或 `fmt=` 未指定，它取決於 `attribute::Format`。

如果請求方法為無條件，則HTTP響應狀態為「200 OK」 `GET` 或 `HEAD`。

伺服器可以以狀態「304」（未修改）答復，並且不返回任何影像資料以響應條件 `GET` 請求(與 [!DNL If-Modified-Since] 欄位 `request-header`)。
