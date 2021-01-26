---
description: 如果將javascript指定為回應格式，則回覆資料的格式會被解析為JavaScript包含檔案。
seo-description: 如果將javascript指定為回應格式，則回覆資料的格式會被解析為JavaScript包含檔案。
seo-title: JavaScript屬性
solution: Experience Manager
title: JavaScript屬性
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# JavaScript屬性{#javascript-properties}

如果將javascript指定為回應格式，則回覆資料的格式會被解析為JavaScript包含檔案。

典型的JavaScript屬性回應具有以下一般結構：

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* 可能是空的。在每行的開始和結束處以及=分隔符號的前後，空格是可選的。 所有值都用單引號括住。 字串中的單引號以兩個連續的單引號逸出。

要解析JavaScript屬性響應，必須在載入屬性檔案之前建立響應中引用的任何對象。 以下是使用`req=props`在JavaScript中取得回應影像大小的範例：

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

