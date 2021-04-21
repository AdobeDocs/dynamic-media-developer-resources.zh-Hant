---
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
title: CallToAction.direction
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 4%

---

# CallToAction.direction{#calltoaction-direction}

互動式視訊檢視器的設定屬性。

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> 指定縮圖在檢視中填入的方式。 </p> <p>設為<span class="codeph"> left </span>以設定從左到右的填色順序。 </p> <p>設為<span class="codeph">右</span>會反轉順序，使檢視以從右到左、從上到下的方向填滿。 </p> <p>設定為<span class="codeph"> auto </span>，當語言環境設定為<span class="codeph"> "ja" </span>時，使元件應用右模式；否則，會使用<span class="codeph">左側的</span>。 </p> </td> 
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
