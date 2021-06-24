---
description: 影像檔案路徑。
solution: Experience Manager
title: 路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 4%

---

# 路徑{#path}

影像檔案路徑。

與此目錄記錄關聯的源影像檔案的相對或絕對路徑和名稱。 伺服器使用管理源資料中所述的路徑解析規則來查找資料檔案。

## 屬性 {#path-properties}

文字字串。 影像記錄需要，範本記錄可能為空。 如果指定，則必須是有效的相對或絕對映像伺服器檔案路徑。 屬性：：如果沒有檔案尾碼，則附加DefaultExt。

## 支援的影像檔案格式 {#path-supported-image-file-formats}

有關支援的檔案格式的完整清單，請參閱影像轉換器(IC)實用程式的說明。

使用Dynamic Media金字塔TIFF(PTIFF)多解析度格式時，需要多個不同解析度的影像資料的應用程式效能最佳。 IC實用程式用於從任何支援的影像格式建立PTIFF影像。

## 預設 {#path-default}

無。

## 另請參閱 {#path-seealso}

[IC實用程式](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [屬性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [屬性：:DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) ,  [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
