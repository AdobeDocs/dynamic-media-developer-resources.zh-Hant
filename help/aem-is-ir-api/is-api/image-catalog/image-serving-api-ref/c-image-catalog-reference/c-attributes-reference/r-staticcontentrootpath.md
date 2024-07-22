---
description: 靜態內容資料根路徑。 此影像目錄之靜態內容資料的根資料夾的絕對路徑或相對路徑區段。
solution: Experience Manager
title: staticcontentrootpath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55ca44cd-4330-47e6-94cc-58c078d34bbd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 2%

---

# staticcontentrootpath{#staticcontentrootpath}

靜態內容資料根路徑。 此影像目錄之靜態內容資料的根資料夾的絕對路徑或相對路徑區段。

請參閱[管理Source資料](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)，以取得伺服器根路徑的其他資訊。

## 屬性 {#section-f8e3986096294b36948d43aafdc3e795}

文字字串。 必須為空白、有效的相對檔案路徑區段或絕對路徑。 不應包含前置和結尾路徑元素分隔字元。

## 預設 {#section-0f741f90fd8d4758a43162c2b5c8a3a3}

如果未定義，則繼承自`default::StaticContentsRootPath`。 如果已定義但空白，則不會對來源檔案根路徑產生任何影響。

## 另請參閱 {#section-9af8846d20d242789df67877f84ed8a7}

[PS：：staticContent.rootPaths](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-staticcontentrootpath.md#reference-a2b5368d078349828d282357681bb2a5) ， [管理Source資料](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)
