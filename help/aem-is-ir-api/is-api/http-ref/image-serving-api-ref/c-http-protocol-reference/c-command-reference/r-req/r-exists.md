---
description: 影像存在。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

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
