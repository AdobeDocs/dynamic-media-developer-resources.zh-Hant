---
description: Video360檢視器的設定屬性。
solution: Experience Manager
title: Video360Player.singleclick
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 9%

---


# Video360Player.singleclick{#video-player-singleclick}

Video360檢視器的設定屬性。

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 設定單鍵／點選的對應，以切換播放／暫停。 設為<span class="codeph"> none</span>會停用單鍵／點選以播放／暫停。 如果設為<span class="codeph"> playPause</span>，則按一下視訊會在播放和暫停視訊之間切換。 在某些裝置上，您可以使用原生控制項。 在這種情況下，<span class="codeph">單點按鍵行為將被禁用。</span> </p> </td> 
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

