---
description: 字型量度檔案路徑。 字型量度檔案的路徑和名稱，包括檔案字尾。
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---


# MetricsPath{#metricspath}

字型量度檔案路徑。 字型量度檔案的路徑和名稱，包括檔案字尾。

用於Adobe Type1種字型。 如果未指定，則伺服器將嘗試在主體字型檔案所在的資料夾中查找字型度量檔案。 如果在轉譯時找不到所需的字型量度檔案，就會發生錯誤。

## 屬性 {#section-955268c581574875b05253d9e14544f3}

文字字串。 Adobe Type1檔案為選用。 必須為空或有效的映像伺服器檔案路徑，絕對或相對於`attribute::RootPath`。

## 預設 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

無。

## 另請參閱 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[屬性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
