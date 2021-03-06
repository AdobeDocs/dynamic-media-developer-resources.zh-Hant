---
title: SocialShare.bearing
description: Video360查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f00b2539-3159-487a-b0fa-9589b694c2e6
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

Video360查看器的配置屬性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫的方向。 </p> <p> 當設定為<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>時，面板沿指定方向滾動，無需額外邊界檢查，這會導致外容器對面板進行剪切。 </p> <p>當設為<span class="codeph"> fit-vertical</span>時，元件會先將基礎面板位置移至SocialShare的底部，並嘗試從底部、右側或左側展開面板。 每次嘗試時，元件都會檢查面板是否被外部容器修剪。 如果所有嘗試失敗，元件會嘗試將基板位置移至頂端，並在上、右、左方向重複轉出嘗試。 </p> <p>當設為<span class="codeph"> fit-lateral</span>時，元件使用類似的邏輯。 然而，它會先將底座向右移動，向右、向下和向上移動，然後將底座向左移動，向左、向下和向上移動。 </p> </td> 
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
