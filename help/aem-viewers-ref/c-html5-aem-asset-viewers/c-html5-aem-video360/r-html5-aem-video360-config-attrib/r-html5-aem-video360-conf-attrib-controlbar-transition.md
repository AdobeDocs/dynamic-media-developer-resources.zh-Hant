---
description: Video360檢視器的設定屬性。
seo-description: Video360檢視器的設定屬性。
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: e8c1da96-3533-4d31-9ad3-569a87948ac6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.transition{#controlbar-transition}

Video360檢視器的設定屬性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`Delaytohideduration(`*[, *`延遲隱藏持續時間)`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡化</span> </p> </td> 
   <td colname="col2"> <p> 指定用於顯示或隱藏控制欄及其內容的效果類型。 </p> <p>使用 <span class="codeph"> none</span> 進行即時顯示和隱藏。 使用淡 <span class="codeph"> 入</span> ，提供漸進淡入和淡出效果。 </p> <p>Internet Explorer 8不支援淡化。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 延遲隱藏</span></span> </p> </td> 
   <td colname="col2"> <p>指定控制列在上次滑鼠／觸控事件與時間控制列隱藏之間的時間（以秒為單位）。 </p> <p> 如果設為 <span class="codeph"> -1</span> ，元件不會觸發其自動隱藏效果，而且一律會在畫面上顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 持 <span class="varname"> 續時間</span></span> </p> </td> 
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

