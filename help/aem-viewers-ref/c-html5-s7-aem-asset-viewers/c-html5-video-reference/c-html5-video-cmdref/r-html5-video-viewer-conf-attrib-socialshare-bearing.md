---
description: 視訊檢視器的設定屬性。
seo-description: 視訊檢視器的設定屬性。
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: d7d92d63-a4c2-4bd9-b0fd-fdfd47504a39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SocialShare.bearing{#socialshare-bearing}

視訊檢視器的設定屬性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的投影片動畫方向。 </p> <p> 當設為 <span class="codeph"> 、向下、向左或向</span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>右檢查指定方向時，面板會向上滾出，而不需額外的邊界檢查，這會導致外部容器對面板進行剪裁。 </p> <p>當設為 <span class="codeph"> 最適垂直</span>，元件會先將基本面板位置移至SocialShare的底部，並嘗試從底部、右側或左側推出面板。 每次嘗試時，元件都會檢查面板是否被外部容器剪裁。 如果所有嘗試都失敗，元件會嘗試將基板位置移至頂端，並在頂端、右側和左側重複推出嘗試。 </p> <p>當設為fit- <span class="codeph"> lateral時</span>，元件會使用類似的邏輯。 不過，它會先將基座向右移動，嘗試向右、向下和向上展示方向，然後將基座向左移動，嘗試向左、向下和向上展示方向。 </p> </td> 
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

