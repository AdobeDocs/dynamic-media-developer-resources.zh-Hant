---
description: 目錄記錄標識符
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 7%

---

# Id {#id}

Platform Server查找影像資料檔案中記錄時使用的索引鍵值。

通常是短且唯一的影像識別碼，例如SKU編號，如果SKU有多個影像，則可能有某種影像尾碼。 也可能是更複雜的字串，看起來更像檔案路徑，以支援使用影像伺服輕鬆復原網站。

## 屬性 {#id-properties}

文字字串。 必要. 影像資料表的主索引鍵。 每個目錄：:Id值在表格內必須是唯一的。

## 預設 {#id-default}

無。

## 另請參閱 {#id-seealso}

[屬性：:RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
