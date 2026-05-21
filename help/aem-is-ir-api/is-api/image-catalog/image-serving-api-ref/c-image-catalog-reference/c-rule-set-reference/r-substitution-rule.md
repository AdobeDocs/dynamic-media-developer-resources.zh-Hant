---
description: 替代字串元素。 <rule>元素中的選用專案。
solution: Experience Manager
title: 替代
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
TQID: 'https://experienceleague.adobe.com/ZdC23CxEXKYN0d-h7nM8588KTS5Vy6BTh0kl5Iseq0w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 2%

---

# 替代{#substitution}

替代字串元素。 `<rule>`個元素中的選用專案。

## 屬性 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

無。

## 資料 {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

替代字串。

## 說明 {#section-4a64a93f5e1a4d04a2db19166578bf76}

為路徑或查詢中的相符字串或子字串定義取代字串。

如果模式運算式包含子運算式（以括弧分隔），則第一個相符的子字串會取代為替代字串。 如果模式運算式不包含子運算式，則會取代整個相符的字串。

如果`<expression>`為空白或不存在，則替代字串會附加至路徑或查詢。

如果`<substitution>`為空白，則會移除相符的字串或子字串。 如果未指定`<substitution>`，則不會修改路徑或查詢字串。

>[!NOTE]
>
>在此`<substitution>`專案所屬的`<rule>`，專案中指定`replace="all"`時，輸入字串中的所有符合專案都會被取代。 依預設，只有第一個相符專案會取代為替代字串。

## 注意 {#section-cedf2adabaaf441c9f598fb0ea180246}

替代字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別以`&`和`<`編碼，或是整個字串可包含在XML CDATA區段中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
