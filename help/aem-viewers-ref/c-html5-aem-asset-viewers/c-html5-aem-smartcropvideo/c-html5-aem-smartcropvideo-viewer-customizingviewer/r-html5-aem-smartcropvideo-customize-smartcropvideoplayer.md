---
title: 視訊播放器
description: 智慧型裁切視訊播放器是檢視器中顯示視訊內容的矩形區域。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 視訊播放器{#video-player}

智慧型裁切視訊播放器是檢視器中顯示視訊內容的矩形區域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在播放的視訊尺寸不符合智慧型裁切視訊播放器的尺寸，則視訊內容會置中於智慧型裁切視訊播放器的矩形顯示區域中。

下列CSS類別選取器會控制智慧型裁切視訊播放器的外觀：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

智慧型裁切視訊播放器的&#x200B;**CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p>主檢視的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

如果系統無法播放視訊，顯示的錯誤訊息可能會進行當地語系化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)。

範例 — 將智慧型裁切視訊播放器大小設為512 x 288畫素時，設定為智慧型裁切視訊檢視器。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

隱藏式字幕會放入智慧型裁切視訊播放器內的內部容器中。 該容器的位置由支援的WebVTT定位運運算元控制。 註解文字本身位於該容器內，其樣式由下列CSS類別選取器控制：

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

隱藏式字幕的&#x200B;**CSS屬性**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p>隱藏式字幕文字背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">色彩</span> </p> </td> 
   <td colname="col2"> <p>隱藏式字幕文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字型粗細</span> </p> </td> 
   <td colname="col2"> <p> 隱藏式字幕字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字型大小</span> </p> </td> 
   <td colname="col2"> <p> 隱藏式字幕字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字型系列</span> </p> </td> 
   <td colname="col2"> <p>隱藏式字幕字型。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要在半透明的黑色背景上將隱藏式字幕文字設定為14畫素、淺灰色、Arial®：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

使用下列CSS類別選取器來控制緩衝動畫的外觀：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
```

**等待圖示的CSS屬性**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">左邊界</span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示左邊界，通常減掉圖示寬度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上邊界</span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示上方邊界，通常減去圖示高度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景影像</span> </p> </td> 
   <td colname="col2"> <p> 旋鈕圖稿。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將緩衝動畫設定為寬101畫素、高29畫素：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```