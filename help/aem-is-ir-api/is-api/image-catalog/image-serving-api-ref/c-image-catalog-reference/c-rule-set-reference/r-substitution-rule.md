---
description: 替代字串元素。 在<rule>元素中為可選項。
solution: Experience Manager
title: 替代
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# 替代{#substitution}

替代字串元素。 在`<rule>`元素中為可選項。

## 屬性 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

無。

## 資料 {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

替代字串。

## 說明 {#section-4a64a93f5e1a4d04a2db19166578bf76}

為路徑或查詢中匹配的字串或子字串定義替換字串。

如果模式表達式包含子表達式（用括弧分隔），則第一個匹配的子字串將替換為替代字串。 如果模式運算式不包含子運算式，則會取代整個相符的字串。

如果`<expression>`為空或缺少，則替代字串將附加到路徑或查詢。

如果`<substitution>`為空，則會移除相符的字串或子字串。 如果未指定`<substitution>`，則不會修改路徑或查詢字串。

>[!NOTE]
>
>在`<rule>`（此`<substitution>`元素所屬的元素）中指定`replace="all"`時，將替換輸入字串中的所有匹配項。 預設情況下，只有第一個匹配被替換字串替換。

## 注意 {#section-cedf2adabaaf441c9f598fb0ea180246}

替代字串不得包含常值&lt;和&amp;字元。 這些保留字元可以分別用`&`和`<`進行編碼，或者將整個字串括在XML CDATA部分中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
