---
description: 替代字串元素。 在<rule>元素中為選用。
solution: Experience Manager
title: 替代
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# 替代{#substitution}

替代字串元素。 `<rule>`元素中為可選。

## 屬性 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

無。

## 資料 {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

替代字串。

## 說明 {#section-4a64a93f5e1a4d04a2db19166578bf76}

定義路徑或查詢中相符字串或子字串的取代字串。

如果模式表達式包含子表達式（用括弧分隔），則第一個匹配的子字串將替換為替代字串。 如果模式運算式不包含子運算式，則會取代整個相符字串。

如果`<expression>`為空或不存在，則替代字串將附加到路徑或查詢。

如果`<substitution>`為空，則會移除相符的字串或子字串。 如果未指定`<substitution>`，則不會修改路徑或查詢字串。

>[!NOTE]
>
>在`<rule>`中指定`replace="all"`時，輸入字串中的所有匹配項都會被替換，此`<substitution>`元素所屬的元素是。 預設情況下，只有第一個匹配項會替換為替代字串。

## 注意 {#section-cedf2adabaaf441c9f598fb0ea180246}

替代字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別用`&`和`<`編碼，或整個字串可以用XML CDATA部分括起來：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
