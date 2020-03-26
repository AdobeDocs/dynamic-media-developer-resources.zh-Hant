---
description: 'null'
seo-description: 'null'
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 8e112f3c-8fa6-4c77-94c5-5027275225e7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1countfadeautoHide`*[, *``*][, *``*][, *``*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 當視訊暫停時，可讓IconEffect顯示在視訊上方。 在某些裝置上會使用原生控制項。 在這種情況下，會忽 <span class="codeph"> 略iconeffect</span> 修飾詞。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出現和重新出現的最大次數。 值-1表 <span class="codeph"> 示該圖</span> 標無限期地重新顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 淡 <span class="varname"> 化</span></span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏動畫的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自 <span class="varname"> 動隱藏</span></span> </p> </td> 
   <td colname="col2"> <p> 設定IconEffect在自動隱藏前保持可見的秒數。 也就是說，淡入動畫完成後和淡出動畫開始前的時間。 設定為 <span class="codeph"> 0</span> 會停用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
