---
description: 尾碼請求修飾符字串。 無或多個以「&」字元分隔的Image Serving命令。
solution: Experience Manager
title: 後修飾符
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# 後修飾符{#postmodifier}

尾碼請求修飾符字串。 無或多個以「&amp;」字元分隔的Image Serving命令。

此欄位中的命令始終覆蓋HTTP請求和 `catalog::Modifier`。

`catalog::PostModifier` 如果某些影像需要通常由URL控制的特殊設定，如 `qlt=` 或 `resmode=`。 `catalog::Modifier` 應用於設定映像目錄中的大多數IS命令。

允許在 `catalog::PostModifier`，只要它們在同一目錄或預設目錄中定義。 自定義變數也可以使用。

>[!NOTE]
>
>如果請求涉及多個層，則僅 `catalog::PostModifier` 的下界。 `catalog::PostModifier` 所有其他層的資料。

## 屬性 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

文本字串。 選擇性.

## 預設 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

無。

## 另請參閱 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[目錄：：修改量](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
