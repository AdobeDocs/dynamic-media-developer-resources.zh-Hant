---
title: 影像
description: 如果要求成功完成，且要求不包含req=命令，或如果req=有下列其中一個值img， debug，則會傳回影像資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# 影像{#images}

如果要求成功完成，且要求不包含req=命令，或如果req=有下列其中一個值，則會傳回影像資料： img、debug

HTTP回應MIME型別是由`fmt=`所決定，或者，如果未指定`fmt=`，則取決於`attribute::Format`的值。

如果要求方法是無條件的`GET`或`HEAD`，則HTTP回應狀態為「200 OK」。

伺服器可能會以狀態&#39;304&#39; （未修改）回覆，且不會傳回任何影像資料以回應條件式`GET`要求（在`request-header`中有[!DNL If-Modified-Since]欄位）。
