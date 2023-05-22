---
title: ControlBar.transition
description: 視頻查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 133717c7-38d9-47b6-86bb-e23ebd8f147a
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

視頻查看器的配置屬性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`延遲隱藏`*[, *`持續時間`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡入</span> </p> </td> 
   <td colname="col2"> <p> 指定用於顯示或隱藏控制欄及其內容的效果類型。 </p> <p>使用 <span class="codeph"> 無</span> 即時展示和隱藏。 使用 <span class="codeph"> 淡</span> 提供漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸漸。 </p> <p>Internet Explorer 8不支援淡出。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 延遲隱藏</span> </span> </p> </td> 
   <td colname="col2"> <p>指定控制欄註冊的上次滑鼠/觸摸事件與控制欄隱藏的時間之間的時間（秒）。 </p> <p> 如果設定為 <span class="codeph"> -1</span>，元件從不觸發其自動隱藏效果，並始終在螢幕上保持可見。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間</span> </span> </p> </td> 
   <td colname="col2"> <p>設定淡入淡出動畫的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
