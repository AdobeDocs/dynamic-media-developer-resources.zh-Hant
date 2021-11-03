---
description: 智慧型裁切視訊播放器是觀看者中顯示視訊內容的矩形區域。
solution: Experience Manager
title: 視訊播放器
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2741821f-78fe-44d4-8604-fee10086e0a0
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 1%

---

# 視訊播放器{#video-player}

智慧型裁切視訊播放器是觀看者中顯示視訊內容的矩形區域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在播放的視訊的尺寸與智慧型裁切視訊播放器的尺寸不符，則視訊內容會置於智慧型裁切視訊播放器的矩形顯示區域中。

下列CSS類別選取器會控制智慧型裁切視訊播放器的外觀：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

**智慧型裁切視訊播放器的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色 </span> </p> </td> 
   <td colname="col2"> <p>主檢視的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

如果系統無法播放視訊，則顯示的錯誤訊息可本地化。 請參閱 [用戶介面元素本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得更多資訊。

範例：若要設定智慧型裁切視訊播放器大小設為512 x 288像素的智慧型裁切視訊檢視器。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

隱藏式字幕會放入智慧型裁切視訊播放器內的內部容器中。 該容器的位置由支援的WebVTT定位操作器控制。 註解文字本身位於該容器內，其樣式由下列CSS類別選取器控制：

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**隱藏式字幕的CSS屬性**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色 </span> </p> </td> 
   <td colname="col2"> <p>隱藏式字幕文本背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>隱藏式字幕文本顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細 </span> </p> </td> 
   <td colname="col2"> <p> 隱藏式字幕字型寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小 </span> </p> </td> 
   <td colname="col2"> <p> 隱藏式字幕字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列 </span> </p> </td> 
   <td colname="col2"> <p>隱藏式字幕字型。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要將隱藏式字幕文本設定為半透明黑色背景上的14像素、淺灰色、Arial:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

緩衝動畫的外觀由以下CSS類選擇器控制：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> 左邊距 </span> </p> </td> 
   <td colname="col2"> <p> 動畫表徵圖左邊距，通常為表徵圖寬度的一半減去。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距上 </span> </p> </td> 
   <td colname="col2"> <p> 動畫表徵圖的頂邊，通常為表徵圖高度的一半減去。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像 </span> </p> </td> 
   <td colname="col2"> <p> 旋鈕圖稿。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要將緩衝動畫設定為101像素寬、29像素高：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
