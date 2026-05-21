---
description: 影像已存在。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
TQID: 'https://experienceleague.adobe.com/JyGNYH5-vW7FbZbMcMk2mQFB7rrrzYd0FpvsBbI-Zi4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 2%

---

# 存在{#exists}

影像已存在。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`*&#x200B;個唯一要求識別碼

傳回名為`catalogRecord.exists`的單一屬性。 如果指定的目錄專案存在於影像或預設目錄中，則屬性值會設為「1」，否則會設為「0」。 針對`/is/content`內容的`req=exists`要求指出靜態內容目錄中是否有指定的記錄。

會忽略請求字串中的其他命令。 HTTP回應可使用以`attribute::NonImgExpiration`為基礎的TTL進行快取。

支援JSONP回應格式的請求可讓您使用`req=`引數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP回應中出現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選擇性. 預設值為`s7jsonResponse`。
