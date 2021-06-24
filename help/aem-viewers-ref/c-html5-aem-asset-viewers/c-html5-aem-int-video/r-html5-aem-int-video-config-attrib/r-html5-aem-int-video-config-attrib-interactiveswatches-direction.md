---
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
title: InteractiveSwatches.direction
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

互動式視訊檢視器的設定屬性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> 指定色票在檢視中的填入方式。 </p> <p>設為<span class="codeph"> left </span>以設定從左到右的填充順序。 </p> <p>設為<span class="codeph">右</span>可反轉順序，使視圖以從右到左、從上到下的方向填充。 </p> <p>設定<span class="codeph"> auto </span>時，當區域設定為" <span class="codeph"> ja </span>"時，元件將應用正確模式；否則，會使用左</span>的<span class="codeph">。 </span></p> </td> 
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
