---
title: ControlBar.transition
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

智慧型裁切視訊檢視器的設定屬性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delayhide`*[, *`持續時間`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡出</span> </p> </td> 
   <td colname="col2"> <p> 指定用於顯示或隱藏控制欄及其內容的效果類型。 </p> <p>使用 <span class="codeph"> 無</span> 即時展示和隱藏。 使用 <span class="codeph"> 淡出</span> 提供漸進漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸。 </p> <p>Internet Explorer 8不支援淡出。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delayhide</span> </span> </p> </td> 
   <td colname="col2"> <p>指定控制欄所登錄的上次滑鼠/觸控事件與時間控制欄隱藏之間的秒數。 </p> <p> 若設為 <span class="codeph"> -1</span>，元件就不會觸發其自動隱藏效果，而且一律會顯示在畫面上。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間</span> </span> </p> </td> 
   <td colname="col2"> <p>設定淡入和淡出動畫的持續時間（以秒為單位）。 </p> </td> 
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
