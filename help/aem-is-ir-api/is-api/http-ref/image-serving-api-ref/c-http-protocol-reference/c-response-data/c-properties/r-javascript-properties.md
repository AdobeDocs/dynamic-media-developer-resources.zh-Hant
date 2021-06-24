---
description: 如果將JavaScript™指定為回應格式，則回覆資料會格式化為JavaScript™包含檔案。
solution: Experience Manager
title: JavaScript™屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# JavaScript™屬性{#javascript-properties}

如果將JavaScript™指定為回應格式，則回覆資料會格式化為JavaScript™包含檔案。

典型的JavaScript™屬性回應具有此一般結構：

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* 可以是空的。每行的開頭和結尾以及=分隔符號前後的空白字元為選用字元。 所有值都以單引號括住。 字串中的單引號會以兩個連續的單引號逸出。

要分析JavaScript™屬性響應，必須在載入屬性檔案之前建立響應中引用的任何對象或對象。 以下是使用`req=props`在JavaScript™中取得回應影像大小的範例：

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
