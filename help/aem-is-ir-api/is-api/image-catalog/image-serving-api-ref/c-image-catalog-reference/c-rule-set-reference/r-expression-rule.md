---
description: 規則運算式圖樣元素。 在<rule>元素中為可選項。
seo-description: 規則運算式圖樣元素。 在<rule>元素中為可選項。
seo-title: 表達式
solution: Experience Manager
title: 表達式
topic: Scene7 Image Serving - Image Rendering API
uuid: f2036015-a2c7-4392-86f6-4cdf3152839a
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 表達式{#expression}

規則運算式圖樣元素。 在元素中為 `<rule>` 選用。

## 屬性 {#section-2d438c889ae84b6da7e0ed84b5d021a0}

無。

## 資料 {#section-e2601008d71243109af1a8c55b58416d}

規則運算式模式字串。

## 說明 {#section-759bfb738ddb45dba1f0807aba8c1113}

元 `<expression>` 素可以是空的或包含簡單搜尋字串或規則運算式模式。 模式會套用至整個請求字串。

當空白或未指定時， `<expression>` 一律會出現相符項目；這等同於指定 `<expression>.*</expression>`。

實施基於Java包 [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)，它提供與Perl類似的規則運算式語法。

## 附註 {#section-10b472a902674893b49ca49a7052c366}

運算式字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別 `&` 使用 `<`和編碼，或將整個字串封入XML區 `CDATA` 段：

`<expression><![CDATA[&fmt=custom]]></expression>`

和標籤之間的所 `<expression>` 有字 `</expression>` 元都會傳遞至規則運算式剖析器，包括選用區段外的字 `CDATA` 元。 應當小心避免額外的空白。

## 另請參閱 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
