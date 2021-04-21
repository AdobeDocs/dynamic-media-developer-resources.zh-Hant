---
description: Postfix要求修飾詞字串。 無或多個以'&'字元分隔的影像伺服指令。
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 4%

---


# PostModifier{#postmodifier}

Postfix要求修飾詞字串。 無或多個以&#39;&amp;&#39;字元分隔的影像伺服指令。

此欄位中的命令始終覆蓋HTTP請求和`catalog::Modifier`中的命令。

`catalog::PostModifier` 當某些影像需要通常由URL控制的特殊設定時(例如 `qlt=` 或 `resmode=`)`catalog::Modifier` 應用於設定映像目錄中的大多數IS命令。

只要宏在相同目錄或預設目錄中定義，`catalog::PostModifier`中就允許使用宏。 自訂變數也可以使用。

>[!NOTE]
>
>如果請求涉及多個層，則僅應用層0的`catalog::PostModifier`內容。 `catalog::PostModifier` 會忽略其他所有圖層。

## 屬性 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

文字字串。 選填。

## 預設 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

無。

## 另請參閱 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[目錄：：修飾詞](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
