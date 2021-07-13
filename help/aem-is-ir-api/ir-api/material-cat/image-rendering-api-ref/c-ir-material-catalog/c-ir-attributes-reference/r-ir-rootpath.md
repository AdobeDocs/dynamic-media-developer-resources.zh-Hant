---
description: 源資料根路徑。 文字字串值。 此影像目錄引用的所有暈映、紋理、影像和ICC資料檔案的根資料夾的絕對路徑或相對路徑段。
solution: Experience Manager
title: RootPath *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# RootPath *{#rootpath}

源資料根路徑。 文字字串值。 此影像目錄引用的所有暈映、紋理、影像和ICC資料檔案的根資料夾的絕對路徑或相對路徑段。

## 屬性 {#section-5ff1cf592dd24dfc8cfa470c753ab828}

文字字串。 必須為空、相對於影像呈現伺服器配置設定`ir.resourceRootPaths`的有效路徑段或有效的絕對檔案路徑。 不應包含前導和尾隨路徑元素分隔字元。

## 預設 {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

若未定義，則繼承自`default::RootPath`。 如果已定義但為空，則不會對源檔案根路徑作出貢獻。

## 另請參閱 {#section-92012cc1ce32448ea977e7e0484857e2}

[目錄：：路徑](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ，目 [錄：:AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969),  `ir.resourceRootPaths`
