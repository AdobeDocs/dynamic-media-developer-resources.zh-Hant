---
description: 規則運算式模式元素。 在<rule>元素中為可選項。
seo-description: 規則運算式模式元素。 在<rule>元素中為可選項。
seo-title: 表達式
solution: Experience Manager
title: 表達式
topic: Scene7 Image Serving - Image Rendering API
uuid: e7ef3769-0090-42d6-8021-1c213f1ee391
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 表達式{#expression}

規則運算式模式元素。 在元素中為 `<rule>` 選用。

## 屬性 {#section-fd0574eee1f9423cbb2ed709c0906800}

無。

## 資料 {#section-4cd740c511a1432da0955e9acfbcf96f}

規則運算式模式字串。

## 說明 {#section-3245c8a531bb455d8398449f6ea63b37}

元 `<expression>` 素可以是空的或包含簡單搜尋字串或規則運算式模式。 模式會套用至整個請求字串。

當空白或未指定時， `<expression>` 一律會出現相符項目；這等同於指定 `<expression>.*</expression>`。

此實作以Java套件 [java.util.regex為基礎](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)，它提供與Perl類似的規則運算式語法。

## 注意 {#section-6b41a900b0ce4a9590e5861e3c81599c}

運算式字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別 `&` 使用 `<`和編碼，或將整個字串封入XML區 `CDATA` 段：

`<expression><![CDATA[&fmt=custom]]></expression>`

和標籤之間的所 `<expression>` 有字 `</expression>` 元都會傳遞至規則運算式剖析器，包括選用區段外的字 `CDATA` 元。 應當小心避免額外的空白。

## 另請參閱 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
