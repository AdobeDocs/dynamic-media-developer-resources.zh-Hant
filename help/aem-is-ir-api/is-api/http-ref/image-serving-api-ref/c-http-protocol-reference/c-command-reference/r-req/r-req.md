---
description: 請求型別。 指定要求的型別。
solution: Experience Manager
title: 需要
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
TQID: 'https://experienceleague.adobe.com/-WzHmELeamQBbVFlzXNKbDE3fKVXw4x6pSoEz0LHav4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 10%

---

# 需要{#req}

請求型別。 指定要求的型別。

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`選項`*]`

* [catalogprops](r-catalogprops.md)
* [存在](r-exists.md)
* [imageprops](r-imageprops.md)
* [影像集](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [地圖](r-map-req.md)
* [遮色片](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [訊息](r-message.md)
* [props](r-props.md)
* [解決](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [設定](r-set.md)
* [目標](r-targets.md)
* [tmb](r-tmb.md)
* [使用者資料](r-userdata.md)
* [驗證](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

除非在詳細描述中另有說明，否則伺服器會傳回MIME型別為`text/plain`的`text`個回應。 許多要求型別可讓您指定回應型別，例如`text`，通常是預設值、`javascript`、`xml`或`json`。 關聯的回應MIME型別分別為`text/plain`、`text/javascript`、`text/xml`和`text/javascript`。

除非另有註明，否則回應會將回應格式化為一組`name=value`配對。

請參閱[屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)。
