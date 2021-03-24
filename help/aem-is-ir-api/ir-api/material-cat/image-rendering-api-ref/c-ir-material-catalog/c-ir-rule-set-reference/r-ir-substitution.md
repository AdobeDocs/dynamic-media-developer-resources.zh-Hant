---
description: 替代字串元素。 在<rule>元素中為可選項。
solution: Experience Manager
title: 替代
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---


# 替代{#substitution}

替代字串元素。 在`<rule>`元素中為可選項。

## 屬性 {#section-d955eefc53eb4274861270669c01f9ca}

無。

## 資料 {#section-a2688866ed6d41279a8478886e511ae3}

替代字串。

## 說明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

為路徑或查詢中匹配的字串或子字串定義替換字串。

如果模式表達式包括子表達式（用括弧分隔），則用替換字串替換第一個匹配的子字串。 如果模式運算式不包含子運算式，則會取代整個相符的字串。

如果`<expression>`為空或缺少，則替代字串將附加到路徑或查詢。

如果`<substitution>`為空，則會移除相符的字串或子字串。 如果未指定`<substitution>`，則不會修改路徑或查詢字串。

## 注意 {#section-90fe89bb17a04804b7ff3c93df082892}

替代字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別編碼為`&`和`<`，或整個字串可封裝為XML `CDATA`區段：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
