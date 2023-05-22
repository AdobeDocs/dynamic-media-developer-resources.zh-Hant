---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|擬垂直|擬側 </span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫方向。 </p> <p> 設定為時 <span class="codeph"> 向上 </span>。 <span class="codeph"> 向下 </span>。 <span class="codeph"> 左 </span>或 <span class="codeph"> 右 </span>，面板在指定方向上滾出而不進行額外邊界檢查。 此行為可能導致外部容器對面板進行剪切。 </p> <p>設定為時 <span class="codeph"> 垂直 </span>，元件首先將基面板位置移到SocialShare的底部，然後嘗試從底部、右側或左側從此基礎位置展開面板。 每次嘗試時，元件都會檢查面板是否被外部容器修剪。 如果所有嘗試都失敗，元件將嘗試將基板位置移到頂部，並從頂部、右側和左側重複部署嘗試。 </p> <p>設定為時 <span class="codeph"> 擬合側 </span>，該元件使用與fit-vertical類似的邏輯。 然而，它將基座向右首次嘗試右、下、上展開方向，然後將基座向左移動，嘗試左、下、上展開方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8e843b967237426e9a8b3cd0f27b9820}

選擇性.

## 預設 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 範例 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
