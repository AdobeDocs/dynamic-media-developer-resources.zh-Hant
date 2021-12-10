---
title: ThumbnailGridView.enabledragging
description: ThumbnailGridView.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '75'
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
   <td> <p> <span class="codeph"> <span class="varname"> 過度拖放值 </span> </span> </p> </td> 
   <td> <p> 函式 <span class="codeph"> 0-1 </span> 範圍。 是 <span class="codeph"> % </span> 值，以在錯誤的實際速度方向上移動。 如果設為 <span class="codeph"> 1 </span>，它會隨滑鼠移動。 如果設為 <span class="codeph"> 0 </span>，它完全不會讓你走錯方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-831c23dea82449bfa50fd155bea365b7}

選填。

## 預設 {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## 範例 {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
