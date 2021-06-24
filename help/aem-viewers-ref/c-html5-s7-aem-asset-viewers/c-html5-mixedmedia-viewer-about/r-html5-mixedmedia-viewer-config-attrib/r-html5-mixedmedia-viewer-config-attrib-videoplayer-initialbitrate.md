---
description: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p>設定用於在案頭上初始播放視頻的視頻的視頻位元速率（以千位/秒為單位）或每秒位元組數。 </p> <p>如果此位元速率值在適用性視訊集中不存在，則視訊播放器會啟動位元速率下一個最低的視訊。 </p> <p>如果設為<span class="codeph"> 0 </span>，視訊播放器會從最低的位元速率開始。 僅適用於不支援HTML5 HLS視訊（在Windows 10上為Firefox、Chrome和Internet Explorer 11瀏覽器）的系統，以及當播放模式設為<span class="codeph">自動</span>時。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
