---
description: 影像存在。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# 存在{#exists}

影像存在。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 唯一請求識別碼

傳回名為`catalogRecord.exists`的單一屬性。 如果指定的目錄條目存在於影像或預設目錄中，則屬性值將設定為&quot;1&quot;，否則將設定為&quot;0&quot;。 `req=exists` 針對內容 `/is/content` 的要求會指出靜態內容目錄中是否有指定的記錄。

請求字串中的其他命令會遭忽略。 HTTP回應可根據`attribute::NonImgExpiration`與TTL快取。

支援JSONP回應格式的要求可讓您使用`req=`參數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式的名稱。僅允許a-z、A-Z和0-9個字元。 選填。預設為 `s7jsonResponse`.
