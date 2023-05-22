---
description: 規則運算式模式元素。 可選 <rule> 元素。
solution: Experience Manager
title: 表達
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---

# 表達{#expression}

規則運算式模式元素。 可選 `<rule>` 元素。

## 屬性 {#section-fd0574eee1f9423cbb2ed709c0906800}

無。

## 資料 {#section-4cd740c511a1432da0955e9acfbcf96f}

規則運算式模式字串。

## 說明 {#section-3245c8a531bb455d8398449f6ea63b37}

的 `<expression>` 元素可以是空的，也可以包含簡單搜索字串或規則運算式模式。 該模式將應用於整個請求字串。

匹配始終出現在 `<expression>` 為空或未指定；這等效於指定 `<expression>.*</expression>`。

該實現基於Java包 [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)，它提供與Perl類似的規則運算式語法。

## 注意 {#section-6b41a900b0ce4a9590e5861e3c81599c}

表達式字串不能包含字面&lt;和&amp;字元。 這些保留字元可以用 `&` 和 `<`，或者整個字串可以用XML括起來 `CDATA` 部分：

`<expression><![CDATA[&fmt=custom]]></expression>`

位於 `<expression>` 和 `</expression>` 標籤將傳遞給規則運算式分析器，包括可選項之外的字元 `CDATA` 的子菜單。 應謹慎避免額外的空白。

## 另請參閱 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
