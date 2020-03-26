---
description: 指定按鈕容器的投影片動畫方向。
seo-description: 指定按鈕容器的投影片動畫方向。
seo-title: FavoritesMenu.bearing
solution: Experience Manager
title: FavoritesMenu.bearing
topic: Dynamic media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

指定按鈕容器的投影片動畫方向。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 當設為 <span class="codeph"> 、向下、向左或向</span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>右方向時，面板不會在指定方向上滾出，而不會進行額外的邊界檢查，這會導致面板被外部容器剪裁。 </p> <p>當設為 <span class="codeph"> fit-vertical</span>時，元件會先將底板位置移至「我的最愛」選單的底部，並嘗試從此底部位置沿下列其中一個方向展開面板：下，右，左。 每次嘗試時，元件都會檢查面板是否被外部容器剪裁。 如果所有嘗試都失敗，元件會嘗試將基板位置移至頂端，並從上、右和左方向重複滾出嘗試。 </p> <p>當設為fit- <span class="codeph"> lateral時</span>，元件會使用類似的邏輯。 基座先向右移動，向右、向下、向上展開。 然後，它把底座向左移動，向左、向下和向上展開。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
