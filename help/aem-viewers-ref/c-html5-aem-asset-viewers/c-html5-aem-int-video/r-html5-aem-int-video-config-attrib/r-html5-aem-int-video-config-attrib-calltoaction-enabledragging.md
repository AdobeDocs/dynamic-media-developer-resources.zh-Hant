---
description: 互動式視訊檢視器的設定屬性。
seo-description: 互動式視訊檢視器的設定屬性。
seo-title: CallToAction.enabledragging
solution: Experience Manager
title: CallToAction.enabledragging
topic: Dynamic media
uuid: efb272b5-e30e-44d5-9dec-0529b1074ed2
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 5%

---


# CallToAction.enabledragging{#calltoaction-enabledragging}

互動式視訊檢視器的設定屬性。

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`過度拖放`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 啟用或停用使用者使用滑鼠或觸控手勢捲動縮圖的能力。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 過度拖放  </span> </span> </p> </td> 
   <td colname="col2"> <p> 位於<span class="codeph"> 0-1 </span>範圍內，它是實際速度在錯誤方向上移動的百分比值。 </p> <p>如果設定為<span class="codeph"> 1 </span>，則它隨滑鼠移動。 </p> <p>如果設定為<span class="codeph"> 0 </span>，則不會讓您向錯誤的方向移動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```

