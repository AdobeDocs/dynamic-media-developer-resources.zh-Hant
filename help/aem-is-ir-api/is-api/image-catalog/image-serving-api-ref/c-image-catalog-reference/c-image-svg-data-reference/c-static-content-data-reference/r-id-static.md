---
title: Id
description: 通常是一個簡短且唯一的識別碼（例如SKU編號），可能帶有某些型別的尾碼，例如SKU具有多個影像或地區設定特有的變數。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
TQID: 'https://experienceleague.adobe.com/xPBbjaHO58J-4HFnChD1ybEVoE2AbRZuFVA8nbquEvg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 3%

---

# Id{#id}

通常是簡短且唯一的識別碼，例如SKU編號，可能具有某種尾碼，例如SKU具有多個影像或地區設定特有的變數。 也可能是更複雜的字串，看起來更像檔案路徑，以支援透過「影像伺服」輕鬆改裝網站。

>[!NOTE]
>
>載入影像目錄時，影像和SVG表格會合併至單一表格。 兩個表格中的ID值必須是唯一的。 如果影像表格包含具有相同ID值的記錄，則會捨棄SVG記錄。 靜態內容是由個別的表格管理；因此，靜態內容專案和影像/SVG專案可能會有相同的ID值。

## 屬性 {#section-874a6853f67b4b229341ca76682884ae}

文字字串。 必要. 影像/SVG或靜態內容資料表的記錄識別碼。 此影像目錄/SVG目錄或此靜態內容目錄中的每個`catalog::Id`值都必須是唯一的，並且不得包含「，」字元。

## 預設 {#section-a26e7d83a5ee44b5918baef82ee48e14}

無。

## 另請參閱 {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute：：RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
