---
title: VideoPlayer.mutevolume
description: 視頻查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 8f644a40-7fd9-4edd-be29-698635b46507
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 9%

---

# VideoPlayer.mutevolume{#videoplayer-mutevolume}

視頻查看器的配置屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]mutevolume=0|1`

<table id="table_2A4F898BBF88417DB0834B7F78637F5D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 設定初始載入時視頻播放的靜音模式。 如果設定為 <span class="codeph"> 1 </span> 卷被靜音；否則，視頻會播放聲音。 在某些設備上，在載入時停止視頻播放還允許視頻自動播放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`mutevolume=1`
