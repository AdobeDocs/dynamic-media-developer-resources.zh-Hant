---
description: 播放圖示覆蓋在主檢視區域上。 它會在暫停視訊或到達視訊結尾時顯示，並且會依據iconeffect參數而定。
seo-description: 播放圖示覆蓋在主檢視區域上。 它會在暫停視訊或到達視訊結尾時顯示，並且會依據iconeffect參數而定。
seo-title: 圖示效果
solution: Experience Manager
title: 圖示效果
topic: Dynamic media
uuid: 81c9c344-5256-4015-8d02-abbf09dca541
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 圖示效果{#icon-effect}

播放圖示覆蓋在主檢視區域上。 它會在暫停視訊或到達視訊結尾時顯示，並且會依據iconeffect參數而定。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

播放圖示的外觀是使用下列CSS類別選擇器來控制：

```
.s7interactivevideoviewer . s7videoplayer .s7iconeffect
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
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
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

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定100 x 100像素的播放圖示。

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

