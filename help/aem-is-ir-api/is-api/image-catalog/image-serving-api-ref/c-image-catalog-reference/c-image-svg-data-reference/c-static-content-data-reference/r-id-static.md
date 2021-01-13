---
description: Id
solution: Experience Manager
title: ID
topic: Scene7 Image Serving - Image Rendering API
uuid: 45a79636-3fa9-4f2a-98bb-a46c9b627dd4
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 5%

---


# Id{#id}

通常是簡短且唯一的識別碼，例如SKU編號，可能帶有某種尾碼，例如SKU具有多個影像或具有特定地區的變化。 也可能是更複雜的字串，看起來更像檔案路徑，以支援使用影像伺服輕鬆改造網站。

>[!NOTE]
>
>當載入影像目錄時，影像和SVG表格會合併為單一表格。 ID值在兩個表格中必須唯一。 如果影像表包含具有相同ID值的記錄，則會捨棄SVG記錄。 靜態內容由單獨的表管理；因此，靜態內容項和影像/SVG項可能具有相同的Id值。

## 屬性 {#section-874a6853f67b4b229341ca76682884ae}

文字字串。 必要. 記錄影像/SVG或靜態內容資料表的標識符。 此影像目錄/SVG目錄或此靜態內容目錄內的每個`catalog::Id`值必須是唯一的，且不得包含&#39;,&#39;字元。

## 預設 {#section-a26e7d83a5ee44b5918baef82ee48e14}

無。

## 另請參閱 {#section-a258d818487d4ee6b7a99a65d18471a9}

[屬性：:RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
