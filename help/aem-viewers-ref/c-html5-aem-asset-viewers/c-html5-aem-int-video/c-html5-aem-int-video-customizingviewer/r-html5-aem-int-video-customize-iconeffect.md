---
description: 播放圖示重疊在主檢視區域上。 它會在視訊暫停或到達視訊結尾時顯示，且也取決於iconeffect參數。
solution: Experience Manager
title: 表徵圖效果
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: bbb35286-fdb6-4329-a837-17fe8f976276
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# 表徵圖效果{#icon-effect}

播放圖示重疊在主檢視區域上。 它會在視訊暫停或到達視訊結尾時顯示，且也取決於iconeffect參數。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

播放圖示的外觀由下列CSS類別選取器控制：

```
.s7interactivevideoviewer . s7videoplayer .s7iconeffect
```

**播放圖示的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p> 播放圖示的顯示影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>。 </p> </td> 
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

表徵圖效果支援`state`屬性選擇器。 `state="play"` 當視訊在播放中間暫停時使用， `state="replay"` 當播放點在資料流結尾時使用。

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定100 x 100像素播放圖示。

```
.s7interactivevideoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7interactivevideoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7interactivevideoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
