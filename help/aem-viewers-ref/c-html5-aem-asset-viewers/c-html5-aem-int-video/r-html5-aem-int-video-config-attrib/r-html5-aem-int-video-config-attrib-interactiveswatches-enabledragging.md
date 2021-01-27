---
description: 互動式視訊檢視器的設定屬性。
seo-description: 互動式視訊檢視器的設定屬性。
seo-title: InteractiveSwatches.enabledragging
solution: Experience Manager
title: InteractiveSwatches.enabledragging
topic: Dynamic Media
uuid: 9a93e6b3-3441-4987-b9e6-a964dbf2247d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 5%

---


# InteractiveSwatches.enabledragging{#interactiveswatches-enabledragging}

互動式視訊檢視器的設定屬性。

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]enabledragging=0|1[, *`過度拖放`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 啟用或停用使用者使用滑鼠或使用觸控手勢捲動色票的能力。 </p> </td> 
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

