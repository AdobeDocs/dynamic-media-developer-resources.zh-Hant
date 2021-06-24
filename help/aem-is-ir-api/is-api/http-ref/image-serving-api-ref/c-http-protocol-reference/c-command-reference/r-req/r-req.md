---
description: 請求類型. 指定要求的類型。
solution: Experience Manager
title: 請求
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 14%

---

# 請求{#req}

請求類型. 指定要求的類型。

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`選項`*]`

* [目錄prop](r-catalogprops.md)
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
* [userdata](r-userdata.md)
* [驗證](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

除非詳細說明中另有說明，否則伺服器會傳回MIME類型為`text/plain`的`text`回應。 許多請求類型都可讓您指定回應類型，例如`text`，通常為預設值： `javascript`、`xml`或`json`。 相關的響應MIME類型分別為`text/plain`、`text/javascript`、`text/xml`和`text/javascript`。

除非另有說明，否則回應會將回應格式化為一組`name=value`配對。

請參閱[屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)。
