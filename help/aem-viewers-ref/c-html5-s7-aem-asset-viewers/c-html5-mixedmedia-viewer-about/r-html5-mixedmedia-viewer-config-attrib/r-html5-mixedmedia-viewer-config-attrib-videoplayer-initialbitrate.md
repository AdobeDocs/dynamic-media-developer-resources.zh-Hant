---
title: VideoPlayer.initialbitrate
description: VideoPlayer.initialbitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
   <td colname="col2"> <p>設定用於案頭上視頻初始回放的視頻比特率（千位/秒或千位/秒）。 </p> <p>如果此比特率值在自適應視頻集中不存在，則視頻播放器將啟動具有下一個最低比特率的視頻。 </p> <p>如果設定為 <span class="codeph"> 0 </span>，視頻播放器從最低可能比特率開始。 僅適用於不支援HTML5 HLS視頻（Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器）的系統，並且當播放模式設定為 <span class="codeph"> 自動 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
