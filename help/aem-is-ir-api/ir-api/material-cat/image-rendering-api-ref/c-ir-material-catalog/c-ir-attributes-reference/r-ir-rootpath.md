---
title: 根路徑
description: Source資料根路徑。 文字字串值。 此影像目錄參照之所有暈映、紋理、影像和ICC資料檔的根資料夾絕對路徑或相對路徑區段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
TQID: 'https://experienceleague.adobe.com/yCtXjcZDG0HCqydirr7TDe5-e0oWtHmlvAxHDl-gfac'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 2%

---

# 根路徑{#rootpath}

Source資料根路徑。 文字字串值。 此影像目錄參照之所有暈映、紋理、影像和ICC資料檔的根資料夾絕對路徑或相對路徑區段。

## 屬性 {#section-5ff1cf592dd24dfc8cfa470c753ab828}

文字字串。 必須為空白、相對於影像演算伺服器組態設定`ir.resourceRootPaths`的有效路徑區段或有效的絕對檔案路徑。 不應包含前置和結尾路徑元素分隔字元。

## 預設 {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

如果未定義，則繼承自`default::RootPath`。 如果已定義但空白，則不會對來源檔案根路徑產生任何影響。

## 另請參閱 {#section-92012cc1ce32448ea977e7e0484857e2}

[目錄：：Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ， [目錄：：AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969)， `ir.resourceRootPaths`
