---
description: 影像檔案路徑。
solution: Experience Manager
title: 路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 4%

---


# 路徑{#path}

影像檔案路徑。

與此目錄記錄關聯的源影像檔案的相對或絕對路徑和名稱。 伺服器使用管理源資料中所述的路徑解析規則查找資料檔案。

## 屬性 {#path-properties}

文字字串。 影像記錄需要，範本記錄可能是空的。 如果指定，則必須是有效的相對或絕對映像伺服器檔案路徑。 attribute::DefaultExt會在未顯示檔案尾碼時附加。

## 支援的影像檔案格式{#path-supported-image-file-formats}

有關支援的檔案格式的完整清單，請參閱映像轉換器(IC)實用程式的說明。

使用Dynamic Media金字塔TIFF(PTIFF)多解析度格式時，需要多種不同解析度的影像資料的應用程式效能最好。 IC公用程式可用來從任何支援的影像格式建立PTIFF影像。

## 預設 {#path-default}

無。

## 另請參閱 {#path-seealso}

[IC實用程式](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ，屬 [性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ，屬 [性：:DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->