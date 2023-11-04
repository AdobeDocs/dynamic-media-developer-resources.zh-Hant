---
description: 字型量度檔案路徑。 字型度量檔案的路徑和名稱，包括檔案字尾。
solution: Experience Manager
title: 量度路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 3%

---

# 量度路徑{#metricspath}

字型量度檔案路徑。 字型度量檔案的路徑和名稱，包括檔案字尾。

用於Adobe Type1字型。 如果未指定，則伺服器會嘗試在主要字型檔案所在的相同資料夾中尋找字型度量檔案。 如果在轉譯時找不到所需的字型量度檔案，則會發生錯誤。

## 屬性 {#section-955268c581574875b05253d9e14544f3}

文字字串。 Adobe Type1檔案則為選用。 必須為空白或有效的影像伺服器檔案路徑，可為絕對或相對 `attribute::RootPath`.

## 預設 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

無。

## 另請參閱 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[屬性：：RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
