---
description: 指定按鈕容器的投影片動畫方向。
solution: Experience Manager
title: FavoritesMenu.bearing
feature: Dynamic Media經典，檢視器，SDK/API,eCatalog
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

指定按鈕容器的投影片動畫方向。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 當設定為<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>時，面板在指定方向滾出而不需額外的邊界檢查，這會導致面板被外部容器夾住。 </p> <p>當設為<span class="codeph"> fit-vertical</span>時，元件會先將底板位置移至「我的最愛」選單的底部，並嘗試從此底部位置沿下列其中一個方向展開面板：下，右，左。 每次嘗試時，元件都會檢查面板是否被外部容器剪裁。 如果所有嘗試都失敗，元件會嘗試將基板位置移至頂端，並從上、右和左方向重複滾出嘗試。 </p> <p>當設為<span class="codeph"> fit-lateral</span>時，元件使用類似的邏輯。 基座先向右移動，向右、向下、向上展開。 然後，它把底座向左移動，向左、向下和向上展開。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
