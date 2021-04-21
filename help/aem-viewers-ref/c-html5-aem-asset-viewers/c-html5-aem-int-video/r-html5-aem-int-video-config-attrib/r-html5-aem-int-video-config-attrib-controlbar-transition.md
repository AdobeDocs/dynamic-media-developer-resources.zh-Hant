---
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

互動式視訊檢視器的設定屬性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`Delaytohideduration(`*[, *`延遲隱藏持續時間)`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡化</span> </p> </td> 
   <td colname="col2"> <p> 指定將用來顯示／隱藏控制列及其內容的效果類型。 </p> <p>設為<span class="codeph"> none</span>以立即顯示／隱藏。 </p> <p>設為<span class="codeph">淡化</span>，提供漸進淡入／淡出效果。 Internet Explorer 8不支援。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> 指定由控制列註冊的上一個滑鼠／觸控事件與時間控制列隱藏之間的秒數時間。 如果設為<span class="codeph"> -1</span>，元件不會觸發其自動隱藏效果，因此一律會在畫面上顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 時段</span></span> </p> </td> 
   <td colname="col2"> <p> 設定淡入／淡出動畫的持續時間，以秒為單位。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
