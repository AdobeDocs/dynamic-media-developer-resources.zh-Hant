---
description: 視訊播放器是觀看者中顯示視訊內容的矩形區域。
solution: Experience Manager
title: 視訊播放器
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,User
exl-id: 9cfeceff-f6bd-42d9-9b85-456bbaa278fd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---

# 視訊播放器{#video-player}

視訊播放器是觀看者中顯示視訊內容的矩形區域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在播放的視訊的維度與視訊播放器的維度不符，視訊內容會置於視訊播放器的矩形顯示區域中。

下列CSS類別選取器會控制視訊播放器的外觀：

```
.s7interactivevideoviewer .s7videoplayer
```

**視訊播放器的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>主檢視的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您可以將系統無法播放視訊時顯示的錯誤訊息當地化。

請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

範例：若要設定視訊播放器大小設為512 x 288像素的視訊檢視器。

```
.s7interactivevideoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

隱藏式字幕會放入視訊播放器內的內部容器中。 該容器的位置由支援的WebVTT定位操作器控制。 註解文字本身位於該容器內，其樣式由下列CSS類別選取器控制：

`.s7interactivevideoviewer .s7videoplayer .s7caption`

**隱藏式字幕的CSS屬性**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>隱藏式字幕文本背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>隱藏式字幕文本顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p> 隱藏式字幕字型寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p> 隱藏式字幕字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>隱藏式字幕字型。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-5b82913ff3c44b7b8187969cb15e9560}

要將隱藏式字幕文本設定為半透明黑色背景上的14像素、淺灰色、Arial:

```
.s7interactivevideoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

緩衝動畫的外觀由以下CSS類選擇器控制：

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon
```

**等待表徵圖的CSS屬性**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 動畫表徵圖寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 動畫表徵圖高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊距  </span> </p> </td> 
   <td colname="col2"> <p> 動畫表徵圖左邊距，通常為表徵圖寬度的一半減去。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距上  </span> </p> </td> 
   <td colname="col2"> <p> 動畫表徵圖的頂邊，通常為表徵圖高度的一半減去。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p> 旋鈕圖稿。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要將緩衝動畫設定為101像素寬、29像素高：

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
