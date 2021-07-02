---
description: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: b156d3f4-c4d3-45fe-b3d3-b7ed38f6eb4d
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> 指定（以每秒kbits或每秒kbps為單位）在當前系統不支援自適應視頻播放的情況下要從自適應視頻集播放的所需視頻比特率。 </p> <p>元件會以最接近（但不超過）指定值的位元速率擷取視訊資料流。 如果適用性視訊集中的所有視訊資料流的品質高於指定值，邏輯會選擇品質最低的位元速率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
