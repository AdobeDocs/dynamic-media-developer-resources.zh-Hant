---
title: CallToAction.enabledragging
description: Interactive Video Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 21db58df-b76e-4a78-afc4-5e0188cb8896
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

---

# CallToAction.enabledragging{#calltoaction-enabledragging}

Interactive Video Viewer的配置屬性。

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`超越`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 啟用或禁用用戶使用滑鼠或使用觸控手勢滾動縮略圖的功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 超越 </span> </span> </p> </td> 
   <td colname="col2"> <p> 在 <span class="codeph"> 0-1 </span> 範圍，它是實際速度錯誤方向上移動的百分比值。 </p> <p>如果設定為 <span class="codeph"> 1 </span>，它隨滑鼠移動。 </p> <p>如果設定為 <span class="codeph"> 0 </span>它不會讓你走錯方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```
