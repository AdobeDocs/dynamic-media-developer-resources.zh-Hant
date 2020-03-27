---
description: 視訊播放器是在檢視器中顯示視訊內容的矩形區域。
seo-description: 視訊播放器是在檢視器中顯示視訊內容的矩形區域。
seo-title: Video360播放器
solution: Experience Manager
title: Video360播放器
topic: Dynamic media
uuid: e78a9c22-4217-42cc-ba47-3acb4130a4fd
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video360 player{#video-player}

視訊播放器是在檢視器中顯示視訊內容的矩形區域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在播放的視訊尺寸不符合視訊播放器的尺寸，則視訊內容會置於視訊播放器的矩形顯示區域內。

下列CSS類別選擇器會控制視訊播放器的外觀：

```
.s7video360viewer .s7video360player
```

**視訊播放器的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>主視圖的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您可以本地化在系統無法播放視訊時顯示的錯誤訊息。

請參 [閱使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

範例——若要設定視訊播放器大小設定為512 x 288像素的視訊檢視器。

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

緩衝動畫的外觀由下列CSS類別選擇器控制：

```
.s7video360viewer .s7video360player .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊距 </span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示的左邊距，通常為圖示寬度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距頂端 </span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示的上邊界，通常為圖示高度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p> 旋鈕圖稿。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——要將緩衝動畫設定為寬101像素、高29像素：

```
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

