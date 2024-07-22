---
title: JavaScript屬性
description: 如果將JavaScript指定為回應格式，則會格式化回覆資料，以便將其剖析為JavaScript&amp；trade； include檔案。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# JavaScript屬性{#javascript-properties}

如果將JavaScript指定為回應格式，則會格式化回覆資料，以便將其剖析為JavaScript包含檔案。

典型的JavaScript屬性回應具有此一般結構：

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`*&#x200B;可以是空的。 每行開頭和結尾以及=分隔符號前後的空白字元為選用。 所有值都以單引號括住。 字串中的單引號會以兩個連續的單引號逸出。

若要剖析JavaScript屬性回應，必須在載入屬性檔案之前建立回應中參考的任何物件。 以下是使用`req=props`在JavaScript中取得回應影像大小的範例：

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
