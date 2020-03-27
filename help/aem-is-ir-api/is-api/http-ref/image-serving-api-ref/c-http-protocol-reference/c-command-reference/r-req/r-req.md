---
description: 請求類型. 指定請求的類型。
seo-description: 請求類型. 指定請求的類型。
seo-title: requin
solution: Experience Manager
title: requin
topic: Scene7 Image Serving - Image Rendering API
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# req{#req}

請求類型. 指定請求的類型。

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`選項`*]`

* [編目prop](r-catalogprops.md)
* [存在](r-exists.md)
* [imageprops](r-imageprops.md)
* [影像集](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [地圖](r-map-req.md)
* [遮罩](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [訊息](r-message.md)
* [props](r-props.md)
* [解決](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [設定](r-set.md)
* [目標](r-targets.md)
* [tmb](r-tmb.md)
* [用戶資料](r-userdata.md)
* [驗證](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

除非詳細說明另有說明，否則伺服器會傳回MIME `text` 類型的回應 `text/plain`。 許多請求類型可讓您指定回應類型， `text`例如通常為預設、 `javascript`、 `xml`或 `json`。 關聯的響應MIME類 `text/plain`型分 `text/javascript`別 `text/xml`是、 `text/javascript`和。

除非另行聲明，否則回應會將回應格式化為一組 `name=value` 對。

請參 [閱屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)。
