---
description: 影像檔案路徑。
solution: Experience Manager
title: 路徑
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0fca88bb-de00-4eff-83ad-c0f5e3b8ece0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# 路徑{#path}

影像檔案路徑。

與此目錄記錄關聯的源影像檔案的相對或絕對路徑和名稱。 伺服器使用管理源資料中所述的路徑解析規則查找資料檔案。

## 屬性 {#path-properties}

文字字串。 影像記錄需要，範本記錄可能是空的。 如果指定，則必須是有效的相對或絕對映像伺服器檔案路徑。 attribute::DefaultExt會在未顯示檔案尾碼時附加。

## 支援的影像檔案格式{#path-supported-image-file-formats}

有關支援的檔案格式的完整清單，請參閱映像轉換器(IC)實用程式的說明。

使用動態媒體金字塔TIFF(PTIFF)多解析度格式時，需要多種不同解析度影像資料的應用程式效果最佳。 IC公用程式可用來從任何支援的影像格式建立PTIFF影像。

## 預設 {#path-default}

無。

## 另請參閱 {#path-seealso}

[IC實用程式](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ，屬 [性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ，屬 [性：:DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->