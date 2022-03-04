---
description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
solution: Experience Manager
title: 元資料欄位類型
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# 元資料欄位類型{#metadata-field-types}

由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。

語法

## 值 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:一個特殊案例 [!DNL `SingleFixedTag`] 不可修改的字典初始化為 [!DNL `True`] 和 [!DNL `False`]。

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:關閉字典中的零個或多個字串值。 只有管理員用戶才能修改字典。
* [!DNL `MultiTag`]:零個或多個字串值。
* [!DNL `SingleFixedTag`]:關閉字典中的單個字串值。 如果 `setAssetMetadata` 或 `batchSetAssetMetadata` 調用的值不在字典中，將返回錯誤。 只有管理員用戶才能修改字典。

* [!DNL `SingleTag`]:任何單字串值。
* [!DNL `String`]
