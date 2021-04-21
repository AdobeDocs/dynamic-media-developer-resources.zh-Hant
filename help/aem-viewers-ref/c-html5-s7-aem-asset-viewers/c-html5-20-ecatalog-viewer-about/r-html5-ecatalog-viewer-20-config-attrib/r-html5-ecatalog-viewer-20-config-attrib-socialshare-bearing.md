---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的投影片動畫方向。 </p> <p> 當設為<span class="codeph"> up </span>、<span class="codeph"> down </span>、<span class="codeph"> left </span>或<span class="codeph"> right </span>時，面板沿指定方向滾出而不需額外的邊界檢查。 此行為可導致外部容器剪裁面板。 </p> <p>當設為<span class="codeph"> fit-vertical </span>時，元件會先將基本面板位置移至SocialShare的底部，並嘗試從底部、右側或左側，從此基本位置展開面板。 每次嘗試時，元件都會檢查面板是否被外部容器剪裁。 如果所有嘗試都失敗，元件會嘗試將基板位置移至頂端，並從上、右和左方向重複展開嘗試。 </p> <p>當設為<span class="codeph"> fit-lateral </span>時，元件會使用與fit-vertical類似的邏輯，但會將底部向右、向下和向上移動第一次嘗試的方向——然後將底部向左移動，嘗試向左、向下和向上移動方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8e843b967237426e9a8b3cd0f27b9820}

選填。

## 預設 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 範例 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
