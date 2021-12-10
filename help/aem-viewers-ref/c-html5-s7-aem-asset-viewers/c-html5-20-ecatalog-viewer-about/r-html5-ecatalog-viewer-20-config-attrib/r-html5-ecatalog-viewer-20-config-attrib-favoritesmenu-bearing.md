---
title: FavoritesMenu.bearing
description: 指定按鈕容器的幻燈片動畫方向。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

指定按鈕容器的幻燈片動畫方向。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 設為時 <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> lef</span>，或 <span class="codeph"> 右</span>，面板沿指定方向滾出，而不需要額外的邊界檢查，這會導致外部容器修剪面板。 </p> <p>設為時 <span class="codeph"> 垂直擬合</span>，元件會先將底板位置移至「我的最愛」功能表的底部。 它會嘗試從此基座位置沿下列其中一個方向展開面板：下，右，左。 每次嘗試時，元件都會檢查面板是否被外部容器修剪。 如果所有嘗試都失敗，元件會嘗試將基板位置移至頂端，並從上、右和左方向重複滾出嘗試。 </p> <p>設為時 <span class="codeph"> 側向擬合</span>，元件會使用類似的邏輯。 底座首先向右移動，向右、向下和向上展開。 然後，它把底座向左移動，嘗試左、下、上滾方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
