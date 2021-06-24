---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`過度拖放值`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> 啟用或停用使用者使用滑鼠或使用觸控手勢捲動色票的能力 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> 過度拖放值  </span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 0-1 </span>範圍內的函式。 它是<span class="codeph"> % </span>值，用於在實際速度的錯誤方向上移動。 如果設定為<span class="codeph"> 1 </span>，則會隨滑鼠移動。 如果設為<span class="codeph"> 0 </span>，則完全不會讓您朝錯誤的方向移動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-831c23dea82449bfa50fd155bea365b7}

選填。

## 預設 {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## 範例 {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
