---
description: 規則運算式模式元素。 在<rule>元素中為可選項。
solution: Experience Manager
title: 表達式
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 4%

---


# expression{#expression}

規則運算式模式元素。 在`<rule>`元素中為可選項。

## 屬性 {#section-fd0574eee1f9423cbb2ed709c0906800}

無。

## 資料 {#section-4cd740c511a1432da0955e9acfbcf96f}

規則運算式模式字串。

## 說明 {#section-3245c8a531bb455d8398449f6ea63b37}

`<expression>`元素可以是空的，或包含簡單搜尋字串或規則運算式模式。 模式會套用至整個請求字串。

當`<expression>`為空或未指定時，一律會出現相符項目；這等同於指定`<expression>.*</expression>`。

實施基於Java軟體包[java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e) ，該軟體包提供與Perl類似的規則運算式語法。

## 注意 {#section-6b41a900b0ce4a9590e5861e3c81599c}

運算式字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別編碼為`&`和`<`，或整個字串可封裝為XML `CDATA`區段：

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`和`</expression>`標籤之間的所有字元都會傳遞至規則運算式剖析器，包括選用`CDATA`區段外的字元。 應當小心避免額外的空白。

## 另請參閱 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
