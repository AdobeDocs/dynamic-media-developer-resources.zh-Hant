---
description: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 3%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
   <td colname="col2"> <p>設定用於在桌上型電腦上播放視訊的視訊位元速率（以千位／秒為單位）或kbps。 </p> <p>如果此位元速率值不存在於最適化視訊集中，則視訊播放器會啟動位元速率下一個最低的視訊。 </p> <p>如果設為<span class="codeph"> 0 </span>，則視訊播放器會從最低位元速率開始。 僅適用於不支援HTML5 HLS視訊的系統（Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器），以及當播放模式設為<span class="codeph">自動</span>時。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
