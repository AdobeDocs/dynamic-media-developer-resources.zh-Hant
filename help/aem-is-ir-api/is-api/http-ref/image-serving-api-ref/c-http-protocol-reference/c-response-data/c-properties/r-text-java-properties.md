---
description: 如果將文本指定為響應格式，則回復資料的格式將設定為可讀為Java屬性。
solution: Experience Manager
title: 文本(Java)屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# 文本(Java)屬性{#text-java-properties}

如果將文本指定為響應格式，則回復資料的格式將設定為可讀為Java屬性。

典型的文本屬性響應具有以下一般結構：

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`* 可能是空的。 在每行的開頭和結尾處以及=分隔符之前和之後，空格是可選的。 單引號或雙引號可用於引起字串值，但不是必需的。

字串值可能包含JAVA樣式轉義字元，如 `\n`。 `\t`。 `\:`或 `\\`。
