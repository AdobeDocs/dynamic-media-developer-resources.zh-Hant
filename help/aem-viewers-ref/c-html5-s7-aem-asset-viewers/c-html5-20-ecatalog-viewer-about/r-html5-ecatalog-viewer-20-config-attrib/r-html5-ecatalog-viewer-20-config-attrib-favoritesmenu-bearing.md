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
ht-degree: 1%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

指定按鈕容器的幻燈片動畫方向。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 上|下|左|右|擬垂直|擬側</span> </p> </td> 
   <td colname="col2"> <p> 設定為時 <span class="codeph"> 向上</span>。 <span class="codeph"> 向下</span>。 <span class="codeph"> 左</span>或 <span class="codeph"> 右</span>，面板在指定方向上滾出而不進行額外邊界檢查，這會導致面板被外部容器夾斷。 </p> <p>設定為時 <span class="codeph"> 垂直</span>，元件首先將基面板位置移到「收藏夾」菜單的底部。 它嘗試從此基地位置沿下列方向之一展開面板：下，右，左。 每次嘗試時，元件都會檢查面板是否被外部容器夾住。 如果所有嘗試都失敗，則元件將嘗試將基板位置移到頂部，並從頂部、右側和左側重複展開嘗試。 </p> <p>設定為時 <span class="codeph"> 擬合側</span>，該元件使用類似的邏輯。 底座首先向右移動，向右、向下和向上展開。 然後，它把底座向左移，試著向左、向下和向上展開方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
