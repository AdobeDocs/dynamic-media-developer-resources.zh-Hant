---
title: Id
description: 通常是一個簡短且唯一的識別碼（例如SKU編號），可能帶有某些型別的尾碼，例如SKU具有多個影像或地區設定特有的變數。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# Id{#id}

通常是簡短且唯一的識別碼，例如SKU編號，可能具有某種尾碼，例如SKU具有多個影像或地區設定特有的變數。 也可能是更複雜的字串，看起來更像檔案路徑，以支援透過「影像伺服」輕鬆改裝網站。

>[!NOTE]
>
>載入影像目錄時，影像和SVG表格會合併至單一表格。 兩個表格中的ID值必須是唯一的。 如果影像表格包含具有相同ID值的記錄，則會捨棄SVG記錄。 靜態內容是由個別的表格管理；因此，靜態內容專案和影像/SVG專案可能會有相同的ID值。

## 屬性 {#section-874a6853f67b4b229341ca76682884ae}

文字字串。 必填。 影像/SVG或靜態內容資料表的記錄識別碼。 此影像目錄/SVG目錄或此靜態內容目錄中的每個`catalog::Id`值都必須是唯一的，並且不得包含「，」字元。

## 預設 {#section-a26e7d83a5ee44b5918baef82ee48e14}

無。

## 另請參閱 {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute：：RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
