---
description: Postfix要求修飾詞字串。 無或多個以「&」字元分隔的「影像伺服」命令。
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 4%

---

# PostModifier{#postmodifier}

Postfix要求修飾詞字串。 無或多個以「&amp;」字元分隔的「影像伺服」命令。

此欄位中的命令始終覆蓋HTTP請求和`catalog::Modifier`中的命令。

`catalog::PostModifier` 如果某些影像需要特殊設定，通常可從URL（例如或）控制，則此功能 `qlt=` 很實 `resmode=`用。`catalog::Modifier` 應用於設定影像目錄中的大多數IS命令。

只要宏在相同目錄或預設目錄中定義，`catalog::PostModifier`中就允許宏。 自訂變數也可供使用。

>[!NOTE]
>
>如果請求涉及多個層，則僅應用層0的`catalog::PostModifier`內容。 `catalog::PostModifier` 會忽略所有其他層。

## 屬性 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

文字字串。 選填。

## 預設 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

無。

## 另請參閱 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[目錄：：修飾詞](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
