---
title: 常見資料類型
description: 目錄屬性和欄位可能包含下列類型之一的資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# 常見資料類型{#common-data-types}

目錄屬性和欄位可能包含下列類型之一的資料。

**色彩**

顏色值。 十六進位的RGB值，可選前面帶0x。 例如，RGB值 `128,255,0` 可指定為 `0x80ff00` 或 `80ff00`。

**標幟**

`0`=false, `1`=true，任何其它值表示未知或未指定。

**枚舉**

`0` 指示未知或未指定的值，與空欄位相同。 有效 `enum` 值是連續的整數，以1開頭。

**整數**

帶符號的整數值(例如 `0, -12, 34`)。 `0` 或者負值可能有特殊意義。

**實數**

帶符號浮點值(例如， `0, 12.5, 245 , -2.34e4`)。 0或負值可能具有特殊含義。

**文本字串**

字串分隔符是可選的，除非字串包含任何 `<CR>`。 `<LF>`或 `<TAB>` 字元。 單引號和雙引號都可以用作分隔符。 如果使用引號，則必須使用兩個連續的引號（例如， &#39;）來轉義字串中嵌入的任何此類引號 `This month''s Special`&#39;)。
