---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,User
exl-id: e93de3b5-b42d-4db8-90b9-9e2aa53af775
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 6%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件預載行為。 </p> <p>設為<span class="codeph"> -1</span>時，當元件初始化或資產變更時，會同時載入縮圖。 </p> <p>設為<span class="codeph"> 0</span>時，只會載入可見的縮圖。 </p> <p>設定<span class="codeph"><span class="varname"> preloadnbr</span></span>定義預載可見區域周圍的不可見行/列的數量。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-a3abd04c03e14c238a07349ce50d8310}

選填。

## 預設 {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## 範例 {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`
