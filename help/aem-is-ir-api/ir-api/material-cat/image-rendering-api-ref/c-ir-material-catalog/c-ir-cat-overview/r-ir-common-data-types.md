---
title: 常見資料型別
description: 目錄屬性和欄位可能包含下列其中一種型別的資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
TQID: 'https://experienceleague.adobe.com/bf3PkSBKhuIzaRglWXs6UH0RoikSPcRUZBIAFdOaHV0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# 常見資料型別{#common-data-types}

目錄屬性和欄位可能包含下列其中一種型別的資料。

**色彩**

色彩值。 十六進位、壓縮的RGB值，可選擇以0x開頭。 例如，RGB值`128,255,0`可以指定為`0x80ff00`或`80ff00`。

**旗標**

`0`=false， `1`=true，任何其他值表示未知或未指定。

**列舉**

`0`表示未知或未指定的值，與空白欄位相同。 有效的`enum`值是從1開始的連續整數。

**整數**

帶正負號的整數值（例如`0, -12, 34`）。 `0`或負值可能有特殊意義。

**實數**

帶正負號的浮點數值（例如，`0, 12.5, 245 , -2.34e4`）。 0或負值可能有特殊意義。

**文字字串**

除非字串包含任何`<CR>`、`<LF>`或`<TAB>`字元，否則字串分隔符號為選用。 單引號與雙引號均可作為分隔符號使用。 如果使用引號，則任何內嵌在字串中的此類引號都必須使用兩個連續引號（例如&#39; `This month''s Special`&#39;）逸出。
