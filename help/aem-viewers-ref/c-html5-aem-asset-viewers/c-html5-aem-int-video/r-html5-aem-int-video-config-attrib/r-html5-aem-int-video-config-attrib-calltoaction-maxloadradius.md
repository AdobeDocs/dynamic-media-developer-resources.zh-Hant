---
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
title: CallToAction.maxloadradius
feature: Dynamic Media經典，檢視器，SDK/API，互動式視訊
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# CallToAction.maxloadradius{#calltoaction-maxloadradius}

互動式視訊檢視器的設定屬性。

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 指定元件預載行為。 </p> <p>當設為<span class="codeph"> -1</span>時，初始化元件或更改資產時，將同時載入所有縮略圖。 </p> <p>設為<span class="codeph"> 0</span>時，僅載入可見的縮圖。 </p> <p>設為<span class="codeph"><span class="varname"> preloadnbr</span></span>，以定義預先載入可見區域周圍的不可見列／欄數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`-1`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```

