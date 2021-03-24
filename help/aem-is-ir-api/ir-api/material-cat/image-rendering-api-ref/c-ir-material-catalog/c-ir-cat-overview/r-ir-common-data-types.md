---
description: 目錄屬性和欄位可包含下列類型之一的資料。
solution: Experience Manager
title: 常見資料類型
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 1%

---


# 常見資料類型{#common-data-types}

目錄屬性和欄位可包含下列類型之一的資料。

**色彩**

顏色值。 十六進位、壓縮的RGB值，可選前置0x。 例如，RGB值`128,255,0`可以指定為`0x80ff00`或`80ff00`。

**標幟**

`0`=false,  `1`=true，任何其他值表示未知或未指定。

**Enum**

0表示未知或未指定的值，與空欄位相同。 有效`enum`值是連續的整數，從1開始。

**整數**

有符號的整數值（例如0、-12、34）。 0或負值可能有特殊意義。

**實數**

已簽署的浮點值(例如`0, 12.5, 245 , -2.34e4`)。 0或負值可能有特殊意義。

**文字字串**

字串分隔字元是選用的，除非字串包含任何`<CR>`、`<LF>`或`<TAB>`字元。 單引號和雙引號可用作分隔字元。 如果使用引號，則嵌入在字串中的任何此類引號都必須通過使用兩個連續引號(如&#39; `This month''s Special`&#39;)。
