---
title: Favoriteview.maxloadradius
description: Favoriteview.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 6bbf75f1-96e7-496d-9f5c-6f449f76bfdd
TQID: 'https://experienceleague.adobe.com/e5J8j5Skr3LZIG-kjfoTwb6-Iu1duI2Lhb6CoDqZ-E8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 58
ht-degree: 5%

---

# Favoriteview.maxloadradius{#favoritesview-maxloadradius}

` [FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 指定元件預先載入行為。 </p> <p>設定為<span class="codeph"> -1</span>時，當初始化元件或變更資產時，將同時載入所有縮圖。 </p> <p>設定為<span class="codeph"> 0</span>時，只會載入可見的縮圖。 </p> <p> 設定為<span class="codeph"><span class="varname"> preloadnbr</span></span>時，您可以指定預先載入可見區域附近的不可見列數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`1`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`maxloadradius=0`
