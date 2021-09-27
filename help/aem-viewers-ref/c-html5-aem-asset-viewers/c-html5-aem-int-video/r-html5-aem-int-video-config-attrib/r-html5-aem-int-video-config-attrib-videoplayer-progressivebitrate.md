---
title: VideoPlayer.progressivebitrate
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 4%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

互動式視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 指定以千位/秒（每秒位元組數）為單位，以在目前系統不支援最適化視訊播放的情況下，從最適化視訊集播放所需的視訊位元速率。 </p> <p>元件會以最接近（但不超過）指定值的位元速率擷取視訊資料流。 如果適用性視訊集中的所有視訊資料流的品質高於指定值，則邏輯會選擇品質最低的位元速率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
