---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7ffdc886-5631-429f-84b4-4b32b715713d
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '75'
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
   <td> <p> <span class="codeph"> <span class="varname"> 過度拖放值 </span> </span> </p> </td> 
   <td> <p> 函式 <span class="codeph"> 0-1 </span> 範圍。 是 <span class="codeph"> % </span> 值，以在錯誤的實際速度方向上移動。 如果設為 <span class="codeph"> 1 </span>，它會隨滑鼠移動。 如果設為 <span class="codeph"> 0 </span>，它完全不會讓你走錯方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0`
