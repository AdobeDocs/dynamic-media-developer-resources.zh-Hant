---
description: 播放圖示覆蓋在主檢視區域上。 它會在暫停視訊或到達視訊結尾時顯示，並且會依據iconeffect參數而定。
solution: Experience Manager
title: 圖示效果
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員
exl-id: e25a3b9d-88ef-4214-9b6b-2527ebf0f145
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# 圖示效果{#icon-effect}

播放圖示覆蓋在主檢視區域上。 它會在暫停視訊或到達視訊結尾時顯示，並且會依據iconeffect參數而定。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

播放圖示的外觀是使用下列CSS類別選擇器來控制：

```
.s7video360viewer . s7video360player .s7iconeffect
```

**播放圖示的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p> 播放圖示的顯示影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 播放圖示的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>播放圖示的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

圖示效果支援`state`屬性選擇器。 `state="play"` 會在播放中間暫停視訊時使用，而在播 `state="replay"` 放磁頭在串流結束時使用。

**範例** -設定100 x 100像素播放圖示。

```
.s7video360viewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
