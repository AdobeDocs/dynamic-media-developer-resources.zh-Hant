---
title: 初始幀
description: 所有查看器通用的參數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---

# 初始幀{#initialframe}

所有查看器通用的參數。

>[!NOTE]
>
>此命令不適用於視頻影像查看器。

` initialFrame= *`幀IDX`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 幀IDX</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定查看器在載入時顯示的基於零的幀索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 頁IDX</span></span> </p> </td> 
   <td colname="col2"> <p>當設備處於縱向方向時，跨頁內頁面的零索引。 對於"從左到右"的環境， <span class="codeph"> 0</span> 表示「左頁」和 <span class="codeph"> 1</span> 表示「右頁」。 對於「從右到左」的環境，情況正好相反： <span class="codeph"> 0</span> 表示「右頁」和 <span class="codeph"> 1</span> 表示「左頁」。 </p> <p>如果未指定， <span class="codeph"> 0</span> 預設情況下為。 設備處於橫向方向時忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選擇性.

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

無預設值。

## 範例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
