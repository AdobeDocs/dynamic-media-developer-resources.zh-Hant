---
description: 視訊檢視器的設定屬性。
seo-description: 視訊檢視器的設定屬性。
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 1ba6f24a-77bb-41ef-a831-a7ac817abd73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1countfadeautoHide`*[, *``*][, *``*][, *``*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 當視訊暫停時，可讓IconEffect顯示在視訊上方。 在某些裝置上會使用原生控制項。 在這種情況下，會忽 <span class="codeph"> 略iconeffect</span> 修飾詞。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出現和重新出現的最大次數。 值-1表 <span class="codeph"> 示該圖</span> 標無限期地重新顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 淡 <span class="varname"> 化</span></span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏動畫的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自 <span class="varname"> 動隱藏</span></span> </p> </td> 
   <td colname="col2"> <p> 設定IconEffect在自動隱藏前保持可見的秒數。 也就是說，淡入動畫完成後和淡出動畫開始前的時間。 設定為 <span class="codeph"> 0</span> 會停用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```

