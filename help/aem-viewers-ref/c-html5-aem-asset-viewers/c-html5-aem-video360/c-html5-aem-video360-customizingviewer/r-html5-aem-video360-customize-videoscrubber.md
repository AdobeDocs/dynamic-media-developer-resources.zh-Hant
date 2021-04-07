---
description: 視訊筆畫是水準滑桿控制項，可讓使用者動態尋找目前播放視訊中的任何時間位置。
solution: Experience Manager
title: 視訊筆刷
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員
exl-id: a0b89b4b-5f66-41d5-88b9-a01fddec437e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 3%

---

# 視頻掃描器{#video-scrubber}

視訊筆畫是水準滑桿控制項，可讓使用者動態尋找目前播放視訊中的任何時間位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

當視訊播放時，Scrubber &#39;knob&#39;也會移動，以指出視訊在播放期間的目前時間位置。 視訊筆畫器一律會取得控制列的整個寬度。 您可將視訊筆畫變成外觀。 使用CSS來變更其高度和垂直位置。

使用下列CSS類別選擇器控制視訊筆畫的一般外觀：

```
.s7video360viewer .s7videoscrubber 
.s7video360viewer .s7videoscrubber .s7videotime 
.s7video360viewer .s7videoscrubber .s7knob
```

**視訊Scrubber的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>從上邊框的位置，包括間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 從底部邊框的位置，包括間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>視訊筆刷的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>視訊筆畫的顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

下列CSS類別選擇器會追蹤背景、播放和載入指標：

```
.s7video360viewer .s7videoscrubber .s7track 
.s7video360viewer .s7videoscrubber .s7trackloaded 
.s7video360viewer .s7videoscrubber .s7trackplayed
```

**音軌的CSS屬性**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>對應軌道的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>對應軌道的顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

下列CSS類別選擇器控制旋鈕：

```
.s7video360viewer .s7videoscrubber .s7knob
```

**旋鈕的CSS屬性**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>垂直旋鈕偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>旋鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>旋鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p>旋鈕圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

下列CSS類別選擇器控制播放的泡泡時間：

```
.s7video360viewer .s7videoscrubber .s7videotime
```

**播放時間泡泡的CSS屬性**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p> 用於顯示時間文字的字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p> 用於顯示時間文字的字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 用於時間顯示文字的字型顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>氣泡區域寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>泡泡區域高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>泡泡區域填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p>氣泡圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>文字與泡泡區域對齊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

視訊筆畫工具提示可以局部化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

**範例** -若要設定視訊檢視器，使用自訂軌道色彩（高度為10像素）來設定視訊檢視器，並從控制列的上邊緣和左邊緣放置10像素和35像素。

```
.s7video360viewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7video360viewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7video360viewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7video360viewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```
