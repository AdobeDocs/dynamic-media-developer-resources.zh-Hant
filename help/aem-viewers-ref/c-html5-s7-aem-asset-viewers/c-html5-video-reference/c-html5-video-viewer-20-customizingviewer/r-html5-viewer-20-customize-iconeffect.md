---
title: 表徵圖效果
description: 該播放表徵圖重疊在主視區上。 它顯示視頻暫停時或視頻結束時的顯示，還取決於影像效果參數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: f4bf343a-4a78-470b-abe5-94e2d608f45d
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# 表徵圖效果{#icon-effect}

該播放表徵圖重疊在主視區上。 它顯示視頻暫停時或視頻結束時的顯示，還取決於影像效果參數。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

播放表徵圖的外觀由以下CSS類選擇器控制：

```
.s7videoviewer . s7videoplayer .s7iconeffect
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
   <td colname="col2"> <p> 如果使用CSS浮雕，則在圖稿浮雕內定位。 </p> <p>請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS繁體 </a>。 </p> </td> 
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

表徵圖效果支援 `state` 屬性選擇器。 當 `state="play"` 在播放中間暫停視頻時使用， `state="replay"` 在播放頭位於流的末尾時使用。

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定100 x 100像素的播放表徵圖。

```
.s7videoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
