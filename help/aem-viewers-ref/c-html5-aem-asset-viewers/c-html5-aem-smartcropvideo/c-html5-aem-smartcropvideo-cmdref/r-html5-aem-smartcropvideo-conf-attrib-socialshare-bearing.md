---
title: SocialShare.bearing
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ef45ba40-661c-4898-a4df-6293ad799a79
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

智慧型裁切視訊檢視器的設定屬性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上|下|左|右|fit — 垂直|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫方向。 </p> <p> 當設定為<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>時，面板會以指定方向轉出，而不需要額外的邊界檢查，這可能會導致面板被外部容器剪裁。 </p> <p>設定為<span class="codeph"> fit-vertical</span>時，元件會先將基礎面板位置移至SocialShare的底部，並嘗試從此類基礎位置從底部、右側或左側轉出面板。 每次嘗試時，元件都會檢查面板是否被外部容器裁剪。 如果所有嘗試都失敗，元件會嘗試將基礎面板位置移至頂端，並在頂端、右側和左側重複轉出嘗試。 </p> <p>當設定為<span class="codeph"> fit-lateral</span>時，元件會使用類似的邏輯。 但是，它會先將基底向右移動，嘗試向右、向下和向上轉出方向，然後將基底向左移動，嘗試向左、向下和向上轉出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
