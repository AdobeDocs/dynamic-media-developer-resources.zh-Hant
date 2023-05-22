---
description: 請求類型. 指定請求的類型。
solution: Experience Manager
title: 請求
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 15%

---

# 請求{#req}

請求類型. 指定請求的類型。

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`選項`*]`

* [編目道具](r-catalogprops.md)
* [存在](r-exists.md)
* [影像](r-imageprops.md)
* [映像集](r-imageset-req.md)
* [img](r-img.md)
* [載入快取](r-loadcache.md)
* [地圖](r-map-req.md)
* [掩模](r-mask-req.md)
* [mbr集](r-mbrset.md)
* [訊息](r-message.md)
* [props](r-props.md)
* [解決](r-resolve.md)
* [保存到檔案](r-savetofile.md)
* [設定](r-set.md)
* [目標](r-targets.md)
* [TMB](r-tmb.md)
* [用戶資料](r-userdata.md)
* [驗證](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

除非在詳細說明中另有說明，否則伺服器將返回 `text` 具有MIME類型的響應 `text/plain`。 許多請求類型允許您指定響應類型，如 `text`，通常為預設值， `javascript`。 `xml`或 `json`。 關聯的響應MIME類型為 `text/plain`。 `text/javascript`。 `text/xml`, `text/javascript`的下界。

除非另有說明，否則響應將響應格式化為一組 `name=value` 對。

請參閱 [屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)。
