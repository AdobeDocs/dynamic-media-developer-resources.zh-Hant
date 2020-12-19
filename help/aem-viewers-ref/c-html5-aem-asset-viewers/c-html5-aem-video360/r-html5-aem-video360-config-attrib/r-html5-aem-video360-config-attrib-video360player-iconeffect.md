---
description: Video360檢視器的設定屬性。
seo-description: Video360檢視器的設定屬性。
seo-title: Video360Player.iconeffect
solution: Experience Manager
title: Video360Player.iconeffect
topic: Dynamic media
uuid: a0a2f840-e330-4636-8daf-1cd3f2eddf01
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# Video360Player.iconeffect{#video-player-iconeffect}

Video360檢視器的設定屬性。

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *`countfadeauto`*][, *``*][, *`隱藏`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 當視訊處於暫停狀態時，可讓IconEffect顯示在視訊的頂端。 在某些裝置上會使用原生控制項。 在這種情況下，會忽略<span class="codeph"> iconeffect</span>修飾詞。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出現和重新出現的最大次數。 值<span class="codeph"> -1</span>表示圖示無限期地重新顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 淡化</span></span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏動畫的持續時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> 設定IconEffect在自動隱藏前保持完全可見的秒數。 也就是說，在動畫淡入完成後和淡出動畫開始之前的時間。 設為<span class="codeph"> 0</span>以停用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
