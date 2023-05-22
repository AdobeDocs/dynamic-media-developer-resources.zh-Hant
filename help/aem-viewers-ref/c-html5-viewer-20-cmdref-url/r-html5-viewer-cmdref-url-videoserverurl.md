---
title: 視頻伺服器URL
description: 所有查看器通用的參數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# 視頻伺服器URL{#videoserverurl}

所有查看器通用的參數。

>[!NOTE]
>
>此命令不適用於視頻影像查看器。

` videoServerUrl= *`視頻根路徑`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 視頻根路徑</span> </span> </p> </td> 
   <td colname="col2"> <p> 視頻伺服器根路徑。 如果未指定域，則將應用從中提供頁面的域。 應用標準URI路徑解析。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選擇性. 標準軟體作為服務使用不需要。

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 範例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
