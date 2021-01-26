---
description: 影像存在。
seo-description: 影像存在。
seo-title: 存在
solution: Experience Manager
title: 存在
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# 存在{#exists}

影像存在。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 唯一請求識別碼

傳回名為`catalogRecord.exists`的單一屬性。 如果指定的目錄條目存在於映像或預設目錄中，則屬性值設定為&quot;1&quot;，否則設定為&quot;0&quot;。 `req=exists` 針對上下文 `/is/content` 的請求將指示靜態內容目錄中是否存在指定的記錄。

請求字串中的其他命令會被忽略。 HTTP響應基於`attribute::NonImgExpiration`可以與TTL進行快取。

支援JSONP回應格式的請求可讓您使用`req=`參數的擴充語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.
