---
description: 替代字串元素。 可選 <rule> 元素。
solution: Experience Manager
title: 替代
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---

# 替代{#substitution}

替代字串元素。 可選 `<rule>` 元素。

## 屬性 {#section-d955eefc53eb4274861270669c01f9ca}

無。

## 資料 {#section-a2688866ed6d41279a8478886e511ae3}

替代字串。

## 說明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

為路徑或查詢中匹配的字串或子字串定義替換字串。

如果模式表達式包含子表達式（用括弧分隔），則第一個匹配的子字串將替換為替換字串。 如果模式表達式不包括子表達式，則替換整個匹配字串。

如果 `<expression>` 為空或不存在，替換字串將附加到路徑或查詢。

如果 `<substitution>` 為空，將刪除匹配的字串或子字串。 如果 `<substitution>` 未指定，則不修改路徑或查詢字串。

## 注意 {#section-90fe89bb17a04804b7ff3c93df082892}

替代字串不能包含字面&lt;和&amp;字元。 這些保留字元可以用 `&` 和 `<`，或者整個字串可以用XML括起來 `CDATA` 部分：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
