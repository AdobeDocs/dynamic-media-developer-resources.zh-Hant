---
description: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: 8371cb69-4cd9-457b-bd8c-e4167fc67600
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 當視訊暫停時，讓IconEffect顯示在視訊的頂端。 在某些裝置上會使用原生控制項。 在這種情況下，會忽略<span class="codeph"> iconeffect</span>修飾元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 計數</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出現和重新出現的次數上限。 值<span class="codeph"> -1</span>表示圖示已無限期地重新顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡出</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏動畫的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> 設定IconEffect在自動隱藏前保持可見的秒數。 即，淡出動畫完成後和淡出動畫開始前的時間。 <span class="codeph"> 0</span>的設定禁用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
