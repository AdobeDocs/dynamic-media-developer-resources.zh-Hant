---
title: SocialShare.bearing
description: 視頻查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

視頻查看器的配置屬性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|擬垂直|擬側</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫方向。 </p> <p> 設定為時 <span class="codeph"> 向上</span>。 <span class="codeph"> 向下</span>。 <span class="codeph"> 左</span>或 <span class="codeph"> 右</span>，面板在指定方向上滾出而不進行額外的邊界檢查，這可能導致面板被外部容器夾斷。 </p> <p>設定為時 <span class="codeph"> 垂直</span>，元件首先將基面板位置移到SocialShare的底部，並嘗試從此基礎位置從底部、右側或左側展開面板。 每次嘗試時，元件都會檢查面板是否被外部容器夾住。 如果所有嘗試都失敗，元件將嘗試將基板位置移到頂部，並在頂部、右側和左側重複部署嘗試。 </p> <p>設定為時 <span class="codeph"> 擬合側</span>，該元件使用類似的邏輯。 但是，它首先將基礎向右移動，嘗試右、下和上展示方向，然後將基礎向左移動，嘗試左、下和上展示方向。 </p> </td> 
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
