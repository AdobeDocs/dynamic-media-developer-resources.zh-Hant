---
description: Video360檢視器的設定屬性。
solution: Experience Manager
title: Video360Player.iconeffect
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員
exl-id: 818ea14b-4dab-4447-9645-46f2ba82547b
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

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
