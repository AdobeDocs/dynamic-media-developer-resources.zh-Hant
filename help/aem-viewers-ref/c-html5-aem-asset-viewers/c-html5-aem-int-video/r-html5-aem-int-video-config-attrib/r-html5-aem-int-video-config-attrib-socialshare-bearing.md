---
title: SocialShare.bearing
description: Interactive Video Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

Interactive Video Viewer的配置屬性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|擬垂直|擬側</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫方向。 設定為時 <span class="codeph"> 向上</span>。 <span class="codeph"> 向下</span>。 <span class="codeph"> 左</span>或 <span class="codeph"> 右</span>，該面板在指定方向上滾出而不進行任何附加邊界檢查，這可能導致面板被外部容器夾住。 </p> <p>設定為時 <span class="codeph"> 垂直</span>，元件首先將基面板位置移到SocialShare的底部。 然後，它嘗試從這樣的基部位置沿下列方向之一展開面板：下，右，左。 每次嘗試時，元件都檢查面板是否被外部容器修剪。 如果所有嘗試都失敗，元件將嘗試將基板位置移到頂部，並從頂部、右側和左側重複部署嘗試。 </p> <p>設定為時 <span class="codeph"> 擬合側</span>，該元件使用類似的邏輯，但首先將基向右移動，然後向右、向下和向上嘗試部署方向。 然後，它把基座向左移，試著左移、下移和上移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```
