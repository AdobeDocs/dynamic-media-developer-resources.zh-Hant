---
description: 互動式視訊檢視器的設定屬性。
seo-description: 互動式視訊檢視器的設定屬性。
seo-title: CallToAction.direction
solution: Experience Manager
title: CallToAction.direction
topic: Dynamic media
uuid: fe182e8f-696d-4515-afdb-49964a374dae
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# CallToAction.direction{#calltoaction-direction}

互動式視訊檢視器的設定屬性。

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> 指定縮圖在檢視中填入的方式。 </p> <p>設為 <span class="codeph"> 左 </span> 側以設定從左至右的填色順序。 </p> <p>設為 <span class="codeph"> 右側 </span> 會反轉順序，讓檢視以從右到左、從上到下的方向填滿。 </p> <p>將設定 <span class="codeph"> 為自 </span> 動，使元件在語言環境設定為「ja」時應用 <span class="codeph"> 正確模式 </span>;否則， <span class="codeph"> 將使 </span> 用左側。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```

