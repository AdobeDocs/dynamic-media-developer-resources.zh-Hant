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
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫方向。 </p> <p> 設為時 <span class="codeph"> up </span>, <span class="codeph"> down </span>, <span class="codeph"> lef </span>，或 <span class="codeph"> 右 </span>，面板沿指定方向滾出，無需額外邊界檢查。 此行為可能導致外部容器剪裁面板。 </p> <p>設為時 <span class="codeph"> 垂直擬合 </span>，元件會先將基本面板位置移至SocialShare的底部，然後嘗試從底部、右側或左側展開面板。 每次嘗試時，元件都會檢查面板是否被外部容器剪下。 如果所有嘗試都失敗，元件會嘗試將基板位置移至頂端，然後從上、右、左方向重複轉出嘗試。 </p> <p>設為時 <span class="codeph"> 側向擬合 </span>，元件會使用與fit-vertical類似的邏輯。 然而，它會將底座右移、下移、上移，然後將底座左移，嘗試左移、下移和上移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8e843b967237426e9a8b3cd0f27b9820}

選填。

## 預設 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 範例 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
