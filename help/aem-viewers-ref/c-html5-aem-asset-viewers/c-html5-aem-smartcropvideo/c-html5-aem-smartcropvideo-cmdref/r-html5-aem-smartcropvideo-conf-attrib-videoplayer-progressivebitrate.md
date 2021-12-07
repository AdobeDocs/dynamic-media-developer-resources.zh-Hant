---
title: SmartCropVideoPlayer.progressivebitrate
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---

# SmartCropVideoPlayer.progressivebitrate{#smartcropvideoplayer-progressivebitrate}

智慧型裁切視訊檢視器的設定屬性。

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 指定在當前系統不支援自適應視訊播放時，從最適化視訊集播放所需的視訊位元速率（以千位/秒或千位/秒為單位）。 </p> <p>元件會以最接近（但不超過）指定值的位元速率擷取視訊資料流。 如果適用性視訊集中的所有視訊資料流的品質高於指定值，邏輯會選擇品質最低的位元速率。 </p> </td> 
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
