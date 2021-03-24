---
description: Video360檢視器的設定屬性。
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

Video360檢視器的設定屬性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`Delaytohideduration(`*[, *`延遲隱藏持續時間)`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡化</span> </p> </td> 
   <td colname="col2"> <p> 指定用於顯示或隱藏控制欄及其內容的效果類型。 </p> <p>使用<span class="codeph"> none</span>來立即顯示和隱藏。 使用<span class="codeph">淡化</span>提供漸進淡入和淡出效果。 </p> <p>Internet Explorer 8不支援淡化。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>指定控制列在上次滑鼠／觸控事件與時間控制列隱藏之間的時間（以秒為單位）。 </p> <p> 如果設為<span class="codeph"> -1</span>，元件不會觸發其自動隱藏效果，而且一律會在畫面上顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間</span> </span> </p> </td> 
   <td colname="col2"> <p>設定淡入和淡出動畫的持續時間，以秒為單位。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```

