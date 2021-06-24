---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: 7ffdc886-5631-429f-84b4-4b32b715713d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`過度拖放值`*]`

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

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0`
