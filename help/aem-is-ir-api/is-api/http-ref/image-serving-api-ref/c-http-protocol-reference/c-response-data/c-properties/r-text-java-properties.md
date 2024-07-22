---
description: 如果指定文字做為回應格式，回覆資料的格式會設定為Java屬性以供讀取。
solution: Experience Manager
title: 文字(Java)屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# 文字(Java)屬性{#text-java-properties}

如果指定文字做為回應格式，回覆資料的格式會設定為Java屬性以供讀取。

典型的文字屬性回應具有此一般結構：

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

*`propertyValue`*&#x200B;可能為空白。 每行開頭和結尾以及=分隔符號前後的空白字元為選用。 單引號或雙引號可用來將字串值括住，但並非必要。

字串值可包含JAVA樣式的逸出字元，例如`\n`、`\t`、`\:`或`\\`。
