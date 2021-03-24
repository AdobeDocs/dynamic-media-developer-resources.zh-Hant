---
description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
solution: Experience Manager
title: 中繼資料欄位類型
feature: Dynamic Media經典，SDK/API，中繼資料
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
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
* [!DNL `SingleFixedTag`]:封閉字典中的單一字串值。如果`setAssetMetadata`或`batchSetAssetMetadata`是以字典中未包含的值呼叫，則會傳回錯誤。 只有管理員使用者可以修改字典。

* [!DNL `SingleTag`]:任何單一字串值。
* [!DNL `String`]

