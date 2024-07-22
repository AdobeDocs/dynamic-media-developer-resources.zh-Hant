---
title: InteractiveSwatches.direction
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 4%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

互動式視訊檢視器的設定屬性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自動|靠左|靠右</span> </p> </td> 
   <td colname="col2"> <p> 指定色票在檢視中填入的方式。 </p> <p>設定為<span class="codeph">左</span>以設定由左至右的填入順序。 </p> <p>設定為<span class="codeph"> right </span>會反轉順序，因此檢視會以由右至左、由上到下的方向填入。 </p> <p>設定<span class="codeph">自動</span>時，如果locale設為" <span class="codeph"> ja </span>"，元件會套用right模式；否則，會使用<span class="codeph">左</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
