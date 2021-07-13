---
description: Video360查看器的配置屬性。
solution: Experience Manager
title: Video360Player.singleclick
feature: Dynamic Media Classic，檢視器，SDK/API,360 VR影片
role: Developer,User
exl-id: dfb44ed5-5f4f-4a2c-a3b4-d49502556399
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---

# Video360Player.singleclick{#video-player-singleclick}

Video360查看器的配置屬性。

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 設定單按/點選的對應以切換播放/暫停。 設為<span class="codeph"> none</span>會停用單鍵/點選以播放/暫停。 如果設為<span class="codeph"> playPause</span>，則按一下視訊會在播放和暫停視訊之間切換。 在某些裝置上，您可以使用原生控制項。 在此情況下，會停用<span class="codeph">單點按</span>行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```
