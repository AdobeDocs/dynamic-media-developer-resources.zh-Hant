---
description: Video360檢視器的設定屬性。
solution: Experience Manager
title: Video360Player.progressivebitrate
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 7%

---


# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Video360檢視器的設定屬性。

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 指定在目前系統不支援最適化視訊播放時，從最適化視訊集播放的視訊位元速率(以kbits/秒（或kbps）為單位。 </p> <p>該元件以最接近（但不超過）指定值的位元速率來擷取視訊串流。 如果「最適化視訊集」中的所有視訊串流的品質都高於指定值，則邏輯會選擇品質最低的位元速率。 </p> </td> 
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

