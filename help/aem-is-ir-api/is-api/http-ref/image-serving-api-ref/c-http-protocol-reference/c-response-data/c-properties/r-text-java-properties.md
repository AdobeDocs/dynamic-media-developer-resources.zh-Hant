---
description: 如果將文本指定為響應格式，則回復資料的格式化為可讀為Java屬性。
seo-description: 如果將文本指定為響應格式，則回復資料的格式化為可讀為Java屬性。
seo-title: 文字(Java)屬性
solution: Experience Manager
title: 文字(Java)屬性
topic: Scene7 Image Serving - Image Rendering API
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 文本(Java)屬性{#text-java-properties}

如果將文本指定為響應格式，則回復資料的格式化為可讀為Java屬性。

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

*`propertyValue`* 可能是空的。在每行的開始和結束處以及=分隔符號的前後，空格是可選的。 單引號或雙引號可用來圈住字串值，但不是必要的。

字串值可能包含JAVA樣式的轉義字元，例如`\n`、`\t`、`\:`或`\\`。
