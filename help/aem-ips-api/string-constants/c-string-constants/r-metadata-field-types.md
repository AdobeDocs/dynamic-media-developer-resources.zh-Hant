---
description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
seo-description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
seo-title: 中繼資料欄位類型
solution: Experience Manager
title: 中繼資料欄位類型
topic: Scene7 Image Production System API
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# 中繼資料欄位類型{#metadata-field-types}

由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。

語法

## 值 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:一個特殊的 [!DNL `SingleFixedTag`] 情況，其中一個不可修改的字典初始化為 [!DNL `True`] 值和 [!DNL `False`]。

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:關閉字典中的零個或多個字串值。只有管理員使用者可以修改字典。
* [!DNL `MultiTag`]:零或多個字串值。
* [!DNL `SingleFixedTag`]:封閉字典中的單一字串值。如果`setAssetMetadata`或`batchSetAssetMetadata`被呼叫時的值不在字典中，則會傳回錯誤。 只有管理員使用者可以修改字典。

* [!DNL `SingleTag`]:任何單一字串值。
* [!DNL `String`]

