---
description: Video360查看器的配置屬性。
solution: Experience Manager
title: Video360Player.progressivebitrate
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,Business Practitioner
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 7%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Video360查看器的配置屬性。

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 指定以每秒kbits（或kbps）為單位的所需視訊位元速率，以在目前系統不支援最適化視訊播放時從最適化視訊集播放。 </p> <p>元件會以最接近（但不超過）指定值的位元速率擷取視訊資料流。 如果適用性視訊集中的所有視訊資料流的品質高於指定值，則邏輯會選擇品質最低的位元速率。 </p> </td> 
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
