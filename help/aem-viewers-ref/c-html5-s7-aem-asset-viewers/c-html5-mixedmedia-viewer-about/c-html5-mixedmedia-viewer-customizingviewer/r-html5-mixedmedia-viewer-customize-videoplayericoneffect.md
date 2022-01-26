---
title: 視頻播放器表徵圖效果
description: 「播放」表徵圖重疊在視頻視圖區域上。 它顯示視頻暫停時或視頻結束時的顯示，還取決於影像效果參數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# 視頻播放器表徵圖效果{#video-player-icon-effect}

「播放」表徵圖重疊在視頻視圖區域上。 它顯示視頻暫停時或視頻結束時的顯示，還取決於影像效果參數。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

播放表徵圖的外觀由以下CSS類選擇器控制：

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**播放表徵圖的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p> 播放表徵圖的顯示影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS浮雕，則在圖稿浮雕內定位。 </p> <p>請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS繁體 </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 播放表徵圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>播放表徵圖的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

表徵圖效果支援 `state` 屬性選擇器。 選擇器 `state="play"` 在播放中間暫停視頻時使用， `state="replay"` 在播放頭位於流的末尾時使用。

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定100 x 100像素的播放表徵圖。

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
