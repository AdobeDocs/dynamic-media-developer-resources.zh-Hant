---
description: FavoritesView.fmt
solution: Experience Manager
title: FavoritesView.fmt
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: d14f8a0c-5fb5-4315-ba8b-79add6d389b0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 5%

---

# FavoritesView.fmt{#favoritesview-fmt}

`[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif|alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件用於從影像伺服器載入影像的影像格式。 格式是影像伺服器和用戶端瀏覽器支援的任何值。 </p> <p>如果影像格式的結尾是<span class="codeph"> -alpha</span>，則元件會將影像呈現為透明內容。 對於所有其他影像格式值，元件會將影像視為不透明。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
