---
description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
solution: Experience Manager
title: 中繼資料欄位類型
feature: Dynamic Media Classic,SDK/API，中繼資料
role: Developer,Administrator
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---

# 中繼資料欄位類型{#metadata-field-types}

由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。

語法

## 值 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:具有初始化為 [!DNL `SingleFixedTag`] 值和的不可修改字典的特 [!DNL `True`] 殊 [!DNL `False`]情況。

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:來自封閉字典的零個或多個字串值。只有管理員使用者可以修改字典。
* [!DNL `MultiTag`]:零個或多個字串值。
* [!DNL `SingleFixedTag`]:封閉字典的單一字串值。如果以字典中不包含的值呼叫`setAssetMetadata`或`batchSetAssetMetadata`，則會傳回錯誤。 只有管理員使用者可以修改字典。

* [!DNL `SingleTag`]:任何單一字串值。
* [!DNL `String`]
