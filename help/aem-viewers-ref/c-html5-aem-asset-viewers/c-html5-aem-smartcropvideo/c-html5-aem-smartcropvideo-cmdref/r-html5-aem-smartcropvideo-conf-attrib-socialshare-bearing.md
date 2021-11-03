---
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

智慧型裁切視訊檢視器的設定屬性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫的方向。 </p> <p> 設為時 <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> lef</span>，或 <span class="codeph"> 右</span>，面板沿指定方向滾出，而不需要進行額外的邊界檢查，這會導致外部容器修剪面板。 </p> <p>設為時 <span class="codeph"> 垂直擬合</span>，元件會先將基礎面板位置移至SocialShare的底部，並嘗試從這類基礎位置從底部、右側或左側展開面板。 每次嘗試時，元件都會檢查面板是否被外部容器修剪。 如果所有嘗試均失敗，元件會嘗試將基板位置移至頂端，並在上、右和左方向重複展開嘗試。 </p> <p>設為時 <span class="codeph"> 側向擬合</span>，元件會使用類似的邏輯。 然而，它會先將底座向右移動，向右、向下和向上移動，然後將底座向左移動，向左、向下和向上移動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
