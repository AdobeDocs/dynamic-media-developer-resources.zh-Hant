---
description: 替代字串元素。 在<rule>元素中為選用。
solution: Experience Manager
title: 替代
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 3%

---

# 替代{#substitution}

替代字串元素。 `<rule>`元素中為可選。

## 屬性 {#section-d955eefc53eb4274861270669c01f9ca}

無。

## 資料 {#section-a2688866ed6d41279a8478886e511ae3}

替代字串。

## 說明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

定義路徑或查詢中相符字串或子字串的取代字串。

如果模式表達式包含子表達式（用括弧分隔），則第一個匹配的子字串將替換為替代字串。 如果模式運算式不包含子運算式，則會取代整個相符字串。

如果`<expression>`為空或不存在，則替代字串將附加到路徑或查詢。

如果`<substitution>`為空，則刪除匹配的字串或子字串。 如果未指定`<substitution>`，則不會修改路徑或查詢字串。

## 注意 {#section-90fe89bb17a04804b7ff3c93df082892}

替代字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別以`&`和`<`編碼，或整個字串可以圍在XML `CDATA`部分中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
