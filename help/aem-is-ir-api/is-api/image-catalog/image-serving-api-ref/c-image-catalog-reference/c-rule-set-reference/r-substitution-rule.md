---
description: 替代字串元素。 可選 <rule> 元素。
solution: Experience Manager
title: 替代
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---

# 替代{#substitution}

替代字串元素。 可選 `<rule>` 元素。

## 屬性 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

無。

## 資料 {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

替代字串。

## 說明 {#section-4a64a93f5e1a4d04a2db19166578bf76}

為路徑或查詢中匹配的字串或子字串定義替換字串。

如果模式表達式包含子表達式（用括弧分隔），則第一個匹配的子字串將替換為替換字串。 如果模式表達式不包括子表達式，則替換整個匹配字串。

如果 `<expression>` 為空或不存在，替換字串將附加到路徑或查詢。

如果 `<substitution>` 為空，將刪除匹配的字串或子字串。 如果 `<substitution>` 未指定，則不修改路徑或查詢字串。

>[!NOTE]
>
>輸入字串中的所有匹配項在 `replace="all"` 在 `<rule>`，元素 `<substitution>` 元素屬於。 預設情況下，只有第一個匹配項被替換為替換字串。

## 注意 {#section-cedf2adabaaf441c9f598fb0ea180246}

替代字串不能包含字面&lt;和&amp;字元。 這些保留字元可以用 `&` 和 `<`，或者整個字串可以括在XML CDATA部分中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
