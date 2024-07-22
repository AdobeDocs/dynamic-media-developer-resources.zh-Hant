---
title: VideoPlayer.iconeffect
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 2%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

互動式視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *`計數`*][, *`淡化`*][, *`自動隱藏`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 啟用當視訊處於暫停狀態時於視訊上方顯示IconEffect。 在某些裝置上，會使用原生控制項。 在這種情況下，會忽略<span class="codeph"> iconeffect</span>修飾元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出現和重新出現的最大次數。 值為<span class="codeph"> -1</span>表示圖示會無限期地重新出現。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">淡化</span></span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏動畫的持續時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">自動隱藏</span></span> </p> </td> 
   <td colname="col2"> <p> 設定IconEffect在自動隱藏前保持完全可見的秒數。 亦即，淡入動畫完成後的時間，以及淡出動畫開始前的時間。 設定為<span class="codeph"> 0</span>以停用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
