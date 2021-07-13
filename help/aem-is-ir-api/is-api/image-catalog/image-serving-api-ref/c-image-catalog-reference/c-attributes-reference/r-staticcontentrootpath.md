---
description: 靜態內容資料根路徑。 此影像目錄靜態內容資料的根資料夾的絕對路徑或相對路徑段。
solution: Experience Manager
title: StaticContentRootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55ca44cd-4330-47e6-94cc-58c078d34bbd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# StaticContentRootPath{#staticcontentrootpath}

靜態內容資料根路徑。 此影像目錄靜態內容資料的根資料夾的絕對路徑或相對路徑段。

有關伺服器根路徑的其他資訊，請參閱[管理源資料](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)。

## 屬性 {#section-f8e3986096294b36948d43aafdc3e795}

文字字串。 必須為空、有效的相對檔案路徑段或絕對路徑。 不應包含前導和尾隨路徑元素分隔字元。

## 預設 {#section-0f741f90fd8d4758a43162c2b5c8a3a3}

若未定義，則繼承自`default::StaticContentsRootPath`。 如果已定義但為空，則不會對源檔案根路徑作出貢獻。

## 另請參閱 {#section-9af8846d20d242789df67877f84ed8a7}

[PS::staticContent.rootPaths](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-staticcontentrootpath.md#reference-a2b5368d078349828d282357681bb2a5) ，管  [理源資料](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)
