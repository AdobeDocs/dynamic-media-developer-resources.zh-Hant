---
description: 指定按鈕容器的幻燈片動畫方向。
solution: Experience Manager
title: FavoritesMenu.bearing
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

指定按鈕容器的幻燈片動畫方向。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 當設定為<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>時，面板沿指定方向滾動，無需進行額外的界限檢查，從而導致外部容器對面板進行剪切。 </p> <p>當設定為<span class="codeph"> fit-vertical</span>時，元件首先將基板位置移到「收藏夾」菜單的底部，並嘗試從該基部位置沿以下方向之一展開面板：下，右，左。 每次嘗試時，元件都會檢查面板是否被外部容器修剪。 如果所有嘗試均失敗，則元件會嘗試將基板位置移至頂部，並從上、右和左方向重複展開嘗試。 </p> <p>當設為<span class="codeph"> fit-lateral</span>時，元件使用類似的邏輯。 底座首先向右移動，向右、向下和向上展開。 然後，它把底座向左移動，嘗試左、下、上滾方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
