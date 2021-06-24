---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: acbcea10-950d-4f98-be5a-5aead9f4e0d9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

[!DNL `[ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

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

[!DNL `1`]

## 範例 {#section-472614b59e04430490a7f16c932bce89}

[!DNL `maxloadradius=0`]
