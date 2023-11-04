---
description: 影像已存在。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 4%

---

# 存在{#exists}

影像已存在。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 唯一要求識別碼

傳回名為的單一屬性 `catalogRecord.exists`. 如果指定的目錄專案存在於影像或預設目錄中，則屬性值會設為「1」，否則會設為「0」。 `req=exists` 針對以下專案的請求： `/is/content` context指示靜態內容目錄中是否有指定記錄。

會忽略請求字串中的其他命令。 HTTP回應可使用以下依據的TTL進行快取： `attribute::NonImgExpiration`.

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱 `req=` 引數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選擇性. 預設為 `s7jsonResponse`.
