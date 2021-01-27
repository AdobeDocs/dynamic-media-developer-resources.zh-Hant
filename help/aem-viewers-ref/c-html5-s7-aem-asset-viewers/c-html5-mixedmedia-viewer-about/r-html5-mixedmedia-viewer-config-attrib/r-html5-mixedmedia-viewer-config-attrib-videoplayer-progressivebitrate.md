---
description: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic Media
uuid: 94de31cd-2b4e-4247-b181-26666767f065
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`值`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 指定（以kbits/秒或kbps為單位）在目前系統不支援最適化視訊播放時，從最適化視訊集播放的視訊位元速率。 </p> <p>該元件會擷取視訊串流，其最接近（但不超過）指定值的位元速率。 如果「最適化視訊集」中的所有視訊串流的品質都高於指定值，則邏輯會選擇品質最低的位元速率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
