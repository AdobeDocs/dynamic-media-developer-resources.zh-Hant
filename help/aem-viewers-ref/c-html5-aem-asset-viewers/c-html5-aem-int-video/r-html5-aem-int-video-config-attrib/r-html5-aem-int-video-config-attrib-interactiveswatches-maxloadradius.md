---
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
feature: Dynamic Media經典，檢視器，SDK/API，互動式視訊
role: 開發人員，商業從業人員
exl-id: 16c9c70a-352d-4a21-bb14-2f9e266a83e8
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

互動式視訊檢視器的設定屬性。

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 指定元件預載行為。 </p> <p>當設為<span class="codeph"> -1</span>時，在初始化元件或更改資產時，將同時載入所有色票。 </p> <p>設為<span class="codeph"> 0</span>時，僅載入可見色票。 </p> <p>設為<span class="codeph"><span class="varname"> preloadnbr</span></span>，以定義預先載入可見區域周圍的不可見列／欄數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
