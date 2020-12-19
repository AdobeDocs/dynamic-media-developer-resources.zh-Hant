---
description: 互動式視訊檢視器的設定屬性。
seo-description: 互動式視訊檢視器的設定屬性。
seo-title: InteractiveSwatches.direction
solution: Experience Manager
title: InteractiveSwatches.direction
topic: Dynamic media
uuid: 08095ab5-f74b-4da6-8f8d-df377995455e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 4%

---


# InteractiveSwatches.direction{#interactiveswatches-direction}

互動式視訊檢視器的設定屬性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> 指定在視圖中填色色色票的方式。 </p> <p>設為<span class="codeph"> left </span>以設定從左到右的填色順序。 </p> <p>設為<span class="codeph">右</span>會反轉順序，使檢視以從右到左、從上到下的方向填滿。 </p> <p>當設定<span class="codeph"> auto </span>時，當locale設定為" <span class="codeph"> ja </span>"時，元件將應用右模式；否則，會使用<span class="codeph">左側的</span>。 </p> </td> 
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

