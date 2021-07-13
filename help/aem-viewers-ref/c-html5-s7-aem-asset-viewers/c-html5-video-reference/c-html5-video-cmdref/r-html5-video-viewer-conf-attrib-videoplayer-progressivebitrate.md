---
description: 視訊檢視器的設定屬性。
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic，檢視器， SDK/API，影片
role: Developer,User
exl-id: 7f9f1bfe-c68f-4ad4-a4a3-e0a8952e07af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 指定（以每秒kbits或每秒kbps為單位）在當前系統不支援自適應視頻播放的情況下要從自適應視頻集播放的所需視頻比特率。 </p> <p>元件會以最接近（但不超過）指定值的位元速率擷取視訊資料流。 如果適用性視訊集中的所有視訊資料流的品質高於指定值，邏輯會選擇品質最低的位元速率。 </p> </td> 
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
