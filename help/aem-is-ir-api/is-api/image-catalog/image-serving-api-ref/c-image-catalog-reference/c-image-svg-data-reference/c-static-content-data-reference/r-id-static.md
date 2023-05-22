---
description: Id
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 4%

---

# Id{#id}

通常是短且唯一的標識符，如SKU編號，可能帶有某種尾碼，例如SKU具有多個影像或具有特定於區域設定的變體。 也可能是一個更複雜的字串，看起來更像檔案路徑，以支援使用Image Serving輕鬆更新網站。

>[!NOTE]
>
>當載入影像目錄時，影像和SVG表合併到單個表中。 ID值必須在兩個表中唯一。 如果影像表包含具有相同ID值的記錄，則SVG記錄將被丟棄。 靜態內容由單獨的表管理；因此，靜態內容項和影像/SVG項可能具有相同的Id值。

## 屬性 {#section-874a6853f67b4b229341ca76682884ae}

文本字串。 必要. 影像/SVG或靜態內容資料表的記錄標識符。 每個 `catalog::Id` 此映像目錄/SVG目錄或此靜態內容目錄中的值必須唯一，且不得包含「，」字元。

## 預設 {#section-a26e7d83a5ee44b5918baef82ee48e14}

無。

## 另請參閱 {#section-a258d818487d4ee6b7a99a65d18471a9}

[屬性：:RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
