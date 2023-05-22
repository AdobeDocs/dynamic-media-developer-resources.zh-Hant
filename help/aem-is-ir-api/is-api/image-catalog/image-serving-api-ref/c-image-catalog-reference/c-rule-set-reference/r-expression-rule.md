---
description: 規則運算式模式元素。 可選 <rule> 元素。
solution: Experience Manager
title: 表達
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 4%

---

# 表達{#expression}

規則運算式模式元素。 可選 `<rule>` 元素。

## 屬性 {#section-2d438c889ae84b6da7e0ed84b5d021a0}

無。

## 資料 {#section-e2601008d71243109af1a8c55b58416d}

規則運算式模式字串。

## 說明 {#section-759bfb738ddb45dba1f0807aba8c1113}

的 `<expression>` 元素可以是空的，也可以包含簡單搜索字串或規則運算式模式。 該模式將應用於整個請求字串。

匹配始終出現在 `<expression>` 為空或未指定；這等效於指定 `<expression>.*</expression>`。

該實現基於Java包 [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)，它提供與Perl類似的規則運算式語法。

## 附註 {#section-10b472a902674893b49ca49a7052c366}

表達式字串不能包含字面&lt;和&amp;字元。 這些保留字元可以用 `&` 和 `<`，或者整個字串可以用XML括起來 `CDATA` 部分：

`<expression><![CDATA[&fmt=custom]]></expression>`

位於 `<expression>` 和 `</expression>` 標籤將傳遞給規則運算式分析器，包括可選項之外的字元 `CDATA` 的子菜單。 應謹慎避免額外的空白。

## 另請參閱 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
