---
description: 互動式視訊檢視器的設定屬性。
seo-description: 互動式視訊檢視器的設定屬性。
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: b3978280-7826-44c0-bd25-357e145121f8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# SocialShare.bearing{#socialshare-bearing}

互動式視訊檢視器的設定屬性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的投影片動畫方向。 當設為 <span class="codeph"> 、向下、向左或向右檢查時</span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>，面板沿指定方向向上滾出，而沒有任何額外的邊界檢查，這可能導致面板被外部容器夾住。 </p> <p>當設為 <span class="codeph"> fit-vertical</span>時，元件會先將基板位置移至SocialShare的底部，並嘗試從此基本位置沿下列其中一個方向展開面板：下，右，左。 每次嘗試時，元件都會檢查面板是否被外部容器剪裁。 如果所有嘗試都失敗，元件會嘗試將基板位置移至頂端，並從頂端、右側和左側重複推出嘗試。 </p> <p>當設為 <span class="codeph"> fit-lateral</span>時，元件會使用類似的邏輯，但會先將底座向右移動，然後向右、向下和向上移出方向。 然後，它將基座向左移動，嘗試左、下和上移方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```

