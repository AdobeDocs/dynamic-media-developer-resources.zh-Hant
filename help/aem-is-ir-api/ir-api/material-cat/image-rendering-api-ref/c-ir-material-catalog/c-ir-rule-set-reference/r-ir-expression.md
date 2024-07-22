---
description: 規則運算式模式元素。 <rule>元素中的選用專案。
solution: Experience Manager
title: 運算式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 5%

---

# 運算式{#expression}

規則運算式模式元素。 `<rule>`個元素中的選用專案。

## 屬性 {#section-fd0574eee1f9423cbb2ed709c0906800}

無。

## 資料 {#section-4cd740c511a1432da0955e9acfbcf96f}

規則運算式模式字串。

## 說明 {#section-3245c8a531bb455d8398449f6ea63b37}

`<expression>`專案可以是空的，或包含簡單的搜尋字串或規則運算式模式。 此模式會套用至整個請求字串。

當`<expression>`為空白或未指定時，一律會有相符專案；這等同於指定`<expression>.*</expression>`。

實作是以Java套件[java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)為基礎，它提供類似於Perl的規則運算式語法。

## 注意 {#section-6b41a900b0ce4a9590e5861e3c81599c}

運算式字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別以`&`和`<`編碼，或是整個字串可包含在XML `CDATA`區段中：

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`與`</expression>`標籤之間的所有字元都會傳遞至規則運算式剖析器，包括選擇性`CDATA`區段以外的字元。 請務必避免出現額外的空白字元。

## 另請參閱 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
