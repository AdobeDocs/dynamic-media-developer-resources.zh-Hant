---
description: Source資料根路徑。 此影像目錄之來源資料的根資料夾的絕對或相對路徑。
solution: Experience Manager
title: 根路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
TQID: 'https://experienceleague.adobe.com/WFDqweSZS1tNJppprC8pJblN-7LBKRM-IHt2Vfj3oW0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 2%

---

# 根路徑{#rootpath}

Source資料根路徑。 此影像目錄之來源資料的根資料夾的絕對或相對路徑。

`RootPath`是文字字串值。 請參閱[管理Source資料](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)，以取得伺服器根路徑的其他資訊。

## 屬性 {#section-b41d7e0ea63143eb8034569706cad0c0}

文字字串。 必須為空白、有效的相對資料夾路徑或影像伺服器可存取的有效絕對路徑。

## 預設 {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

如果未定義，則繼承自`default::RootPath`。 如果已定義但空白，則不會對來源檔案根路徑產生任何影響。

## 另請參閱 {#section-6bf4ffc4987843a9a2dbe81b43076437}

[目錄：：Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ， [目錄：：MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)， [規則集：：PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)， [管理Source資料](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
