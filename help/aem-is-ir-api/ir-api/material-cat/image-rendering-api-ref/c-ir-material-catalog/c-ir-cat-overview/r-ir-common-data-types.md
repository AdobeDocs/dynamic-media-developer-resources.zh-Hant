---
description: 目錄屬性和欄位可包含以下類型之一的資料。
solution: Experience Manager
title: 常見資料類型
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---

# 常見資料類型{#common-data-types}

目錄屬性和欄位可包含以下類型之一的資料。

**色彩**

顏色值。 十六進位、包裝的RGB值，可選前加0x。 例如，RGB值`128,255,0`可以指定為`0x80ff00`或`80ff00`。

**標幟**

`0`=false,  `1`=true，任何其他值表示未知或未指定。

**列舉**

0表示未知或未指定的值，與空白欄位相同。 有效的`enum`值是連續的整數，從1開始。

**整數**

有符號的整數值（例如0、-12、34）。 0或負值可能有特殊意義。

**實數**

有符號的浮點值(例如`0, 12.5, 245 , -2.34e4`)。 0或負值可能有特殊意義。

**文字字串**

字串分隔字元為選用字串，除非字串包含任何`<CR>`、`<LF>`或`<TAB>`字元。 單引號和雙引號可用作分隔字元。 若使用引號，字串中內嵌的任何此類引號都必須使用兩個連續引號來逸出(例如「 `This month''s Special`」)。
