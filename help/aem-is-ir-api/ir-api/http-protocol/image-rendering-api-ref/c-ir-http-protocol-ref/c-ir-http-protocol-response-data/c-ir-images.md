---
description: 如果請求成功完成，並且請求中未包含req=命令，或者如果req=具有以下值之一，則返回影像資料img，調試。
solution: Experience Manager
title: 影像
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---

# 影像{#images}

如果請求成功完成，並且請求中未包含req=命令，或者如果req=具有以下值之一，則返回影像資料：img，除錯

HTTP響應MIME類型由`fmt=`確定，或者，如果未指定`fmt=`，則取決於`attribute::Format`的值。

如果要求方法是無條件`GET`或`HEAD`，則HTTP回應狀態為「200 OK」。

伺服器可以回復狀態為「304」（未修改），並且不返回任何影像資料以響應條件`GET`請求（`request-header`中出現[!DNL If-Modified-Since]欄位）。
