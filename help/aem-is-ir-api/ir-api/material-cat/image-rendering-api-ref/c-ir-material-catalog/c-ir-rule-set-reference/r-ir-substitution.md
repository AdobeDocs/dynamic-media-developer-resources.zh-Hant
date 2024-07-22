---
title: 替代
description: 替代字串元素。 <rule>元素中的選用專案。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---

# 替代{#substitution}

替代字串元素。 `<rule>`個元素中的選用專案。

## 屬性 {#section-d955eefc53eb4274861270669c01f9ca}

無。

## 資料 {#section-a2688866ed6d41279a8478886e511ae3}

替代字串。

## 說明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

為路徑或查詢中的相符字串或子字串定義取代字串。

如果模式運算式包含子運算式（以括弧分隔），則第一個相符的子字串會被取代為替代字串。 如果模式運算式不包含子運算式，則會取代整個相符的字串。

如果`<expression>`為空白或不存在，則替代字串會附加至路徑或查詢。

如果`<substitution>`為空白，則會移除相符的字串或子字串。 如果未指定`<substitution>`，則不會修改路徑或查詢字串。

## 注意 {#section-90fe89bb17a04804b7ff3c93df082892}

替代字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別以`&`和`<`編碼，或是整個字串可包含在XML `CDATA`區段中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
