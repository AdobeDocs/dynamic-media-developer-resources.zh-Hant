---
description: 所有檢視器通用的參數。
solution: Experience Manager
title: initialFrame
feature: Dynamic Media Classic，檢視器，SDK/API
role: Developer,Business Practitioner
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# initialFrame{#initialframe}

所有檢視器通用的參數。

>[!NOTE]
>
>此命令不適用於視頻影像查看器。

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定查看器在載入時顯示的基於零的幀索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>裝置縱向時跨頁內頁面的零索引。 在「left-to-right」環境中<span class="codeph"> 0</span>表示「left page」，而<span class="codeph"> 1</span>表示「right page」。 在「從右到左」中，情況正好相反：<span class="codeph"> 0</span>表示「右頁」，<span class="codeph"> 1</span>表示「左頁」。 </p> <p>如果未指定，預設會假設<span class="codeph"> 0</span>。 當裝置為橫向時，會忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選填。

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

無預設值。

## 範例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
