---
description: 如果將文本指定為響應格式，則回復資料的格式可讀為Java屬性。
solution: Experience Manager
title: 文本(Java)屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 文本(Java)屬性{#text-java-properties}

如果將文本指定為響應格式，則回復資料的格式可讀為Java屬性。

典型文本屬性響應具有以下一般結構：

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

*`propertyValue`* 可能是空的。每行的開頭和結尾以及=分隔符號前後的空白字元為選用字元。 單引號或雙引號可用來括住字串值，但並非必要項目。

字串值可能包含JAVA樣式的逸出字元，如`\n`、`\t`、`\:`或`\\`。
