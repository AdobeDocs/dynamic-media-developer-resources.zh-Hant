---
description: 影像已存在。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---

# 存在{#exists}

影像已存在。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`*&#x200B;個唯一要求識別碼

傳回名為`catalogRecord.exists`的單一屬性。 如果指定的目錄專案存在於影像或預設目錄中，則屬性值會設為「1」，否則會設為「0」。 針對`/is/content`內容的`req=exists`要求指出靜態內容目錄中是否有指定的記錄。

會忽略請求字串中的其他命令。 HTTP回應可使用以`attribute::NonImgExpiration`為基礎的TTL進行快取。

支援JSONP回應格式的請求可讓您使用`req=`引數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP回應中出現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選填。 預設值為`s7jsonResponse`。
