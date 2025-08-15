---
description: Postfix要求修飾元字串。 沒有或多個以「&」字元分隔的「影像伺服」命令。
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# PostModifier{#postmodifier}

Postfix要求修飾元字串。 沒有或多個以「&amp;」字元分隔的「影像伺服」命令。

此欄位中的命令一律會覆寫HTTP要求和`catalog::Modifier`中的命令。

如果某些影像需要特殊設定（通常由URL控制），例如`catalog::PostModifier`或`qlt=`，則`resmode=`會很有用。 `catalog::Modifier`應該用於設定影像目錄中的大多數IS命令。

`catalog::PostModifier`允許使用巨集，只要這些巨集是在相同目錄或預設目錄中定義即可。 您也可以使用自訂變數。

>[!NOTE]
>
>如果要求涉及多個圖層，則僅套用圖層0的`catalog::PostModifier`內容。 已忽略所有其他圖層的`catalog::PostModifier`。

## 屬性 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

文字字串。 選擇性.

## 預設 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

無。

## 另請參閱 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog：：Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
