---
description: 規則運算式模式元素。 在<rule>元素中為選用。
solution: Experience Manager
title: 運算式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 4%

---

# 運算式{#expression}

規則運算式模式元素。 `<rule>`元素中為可選。

## 屬性 {#section-2d438c889ae84b6da7e0ed84b5d021a0}

無。

## 資料 {#section-e2601008d71243109af1a8c55b58416d}

規則運算式模式字串。

## 說明 {#section-759bfb738ddb45dba1f0807aba8c1113}

`<expression>`元素可以為空或包含簡單的搜尋字串或規則運算式模式。 模式會套用至整個請求字串。

當`<expression>`為空或未指定時，始終出現匹配；這等同於指定`<expression>.*</expression>`。

實作以Java套件[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)為基礎，提供與Perl類似的規則運算式語法。

## 附註 {#section-10b472a902674893b49ca49a7052c366}

運算式字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別以`&`和`<`編碼，或整個字串可以圍在XML `CDATA`部分中：

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`和`</expression>`標籤之間的所有字元都會傳遞至規則運算式剖析器，包括選用`CDATA`區段以外的字元。 請謹慎避免出現額外的空白。

## 另請參閱 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
