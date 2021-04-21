---
description: 規則運算式圖樣元素。 在<rule>元素中為可選項。
solution: Experience Manager
title: 表達式
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 4%

---


# expression{#expression}

規則運算式圖樣元素。 在`<rule>`元素中為可選項。

## 屬性 {#section-2d438c889ae84b6da7e0ed84b5d021a0}

無。

## 資料 {#section-e2601008d71243109af1a8c55b58416d}

規則運算式模式字串。

## 說明 {#section-759bfb738ddb45dba1f0807aba8c1113}

`<expression>`元素可以是空的，或包含簡單搜尋字串或規則運算式模式。 模式會套用至整個請求字串。

當`<expression>`為空或未指定時，一律會出現相符項目；這等同於指定`<expression>.*</expression>`。

實施基於Java軟體包[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) ，它提供與Perl類似的規則運算式語法。

## 附註 {#section-10b472a902674893b49ca49a7052c366}

運算式字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別編碼為`&`和`<`，或整個字串可封裝為XML `CDATA`區段：

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`和`</expression>`標籤之間的所有字元都會傳遞至規則運算式剖析器，包括選用`CDATA`區段外的字元。 應當小心避免額外的空白。

## 另請參閱 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
