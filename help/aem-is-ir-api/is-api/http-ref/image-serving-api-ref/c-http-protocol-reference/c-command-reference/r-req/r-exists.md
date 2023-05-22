---
description: 影像存在。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# 存在{#exists}

影像存在。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 唯一請求標識符

返回名為 `catalogRecord.exists`。 如果映像或預設目錄中存在指定的目錄條目，則將屬性值設定為「1」，否則將其設定為「0」。 `req=exists` 對 `/is/content` 上下文將指示靜態內容目錄中是否存在指定記錄。

請求字串中的其他命令將被忽略。 HTTP響應可以與基於的TTL進行快取 `attribute::NonImgExpiration`。

支援JSONP響應格式的請求允許您使用擴展語法指定JS回調處理程式的名稱 `req=` 參數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP響應中存在的JS處理程式的名稱。 只允許使用a-z、A-Z和0-9個字元。 選擇性. 預設為 `s7jsonResponse`.
