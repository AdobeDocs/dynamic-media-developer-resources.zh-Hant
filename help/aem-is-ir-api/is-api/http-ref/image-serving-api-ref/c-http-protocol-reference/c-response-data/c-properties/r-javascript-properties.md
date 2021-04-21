---
description: 如果將JavaScript™指定為回應格式，則回覆資料的格式會被解析為JavaScript™包含檔案。
solution: Experience Manager
title: JavaScript™屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# JavaScript™屬性{#javascript-properties}

如果將JavaScript™指定為回應格式，則回覆資料的格式會被解析為JavaScript™包含檔案。

典型的JavaScript™屬性響應具有以下一般結構：

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* 可以是空的。在每行的開始和結束處以及=分隔符號的前後，空格是可選的。 所有值都用單引號括住。 字串中的單引號以兩個連續的單引號逸出。

要解析JavaScript™屬性響應，必須在載入屬性檔案之前建立響應中引用的任何對象或對象。 以下是使用`req=props`在JavaScript™中取得回應影像大小的範例：

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

