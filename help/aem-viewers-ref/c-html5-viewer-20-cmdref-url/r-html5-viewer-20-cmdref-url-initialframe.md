---
description: 所有檢視器通用的參數。
seo-description: 所有檢視器通用的參數。
seo-title: initialFrame
solution: Experience Manager
title: initialFrame
topic: Dynamic Media
uuid: 5d1c3a8a-8598-47c9-a106-36e8c6fcafb0
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
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
   <td colname="col2"> <p> 指定檢視器在載入時顯示的零架構影格索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>當裝置朝向縱向時，跨頁內頁面的零索引。 在「從左到右」環境中，<span class="codeph"> 0</span>表示「左頁」，而<span class="codeph"> 1</span>表示「右頁」。 在「從右到左」中，情況正好相反：<span class="codeph"> 0</span>表示「右頁」,<span class="codeph"> 1</span>表示「左頁」。 </p> <p>如果未指定，則預設情況下假定<span class="codeph"> 0</span>。 在裝置處於橫向時忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選填。

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

沒有預設值。

## 範例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```

