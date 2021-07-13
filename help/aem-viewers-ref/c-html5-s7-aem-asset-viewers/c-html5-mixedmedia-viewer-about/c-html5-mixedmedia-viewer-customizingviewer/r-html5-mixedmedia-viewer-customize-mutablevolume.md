---
description: 可變音量控制項最初顯示為按鈕，允許用戶將視頻播放器聲音靜音或取消靜音。
solution: Experience Manager
title: 可變音量
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,User
exl-id: 9afa56f9-443c-4307-843c-d7ddba6ec604
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 2%

---

# 可變音量{#mutable-volume}

可變音量控制項最初顯示為按鈕，允許用戶將視頻播放器聲音靜音或取消靜音。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

當用戶翻過按鈕時，會出現一個滑桿，允許用戶設定音量。 可變體積塊控制項可由CSS相對於包含它的控制欄進行大小、外觀和定位。

可變卷區域的外觀由以下CSS類選擇器控制：

```
.s7mixedmediaviewer .s7mutablevolume
```

**可變卷的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p> 從上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p> 從右邊框定位，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 可變音量控制的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>可變體積控制項的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 可變音量控制項的顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

靜音/取消靜音按鈕外觀由下列CSS類別選取器控制：

```
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton
```

您可以控制每個按鈕狀態的背景影像。 按鈕的大小繼承自卷控制項的大小。

**按鈕影像的CSS屬性**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprites </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕同時支援`state`和`selected`屬性選擇器，它們可用於將不同的外觀應用於不同的按鈕狀態。 具體來說，`selected='true'`對應於「靜音」狀態，而`selected='false'`對應於「未靜音」狀態。

垂直卷條區域由以下CSS類選擇器控制：

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume
```

**垂直卷條區域的CSS屬性**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 垂直體積塊的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p> 垂直體積塊的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p> 垂直體積的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

垂直卷控制項內的軌道由以下CSS類選擇器控制：

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**垂直卷控制項的CSS屬性**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 垂直音量控制項的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

垂直音量旋鈕由以下CSS類選擇器控制：

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**垂直音量控制旋鈕的CSS屬性**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p> 垂直音量控制旋鈕圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprites </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制旋鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制旋鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制旋鈕的水準位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) 。

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定32 x 32像素的靜音按鈕，從頂部放置6像素，從控制條的右邊設定38像素。 選取或未選取時，針對四個不同按鈕狀態中的每一個顯示不同的影像。

```
.s7mixedmediaviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

下面是如何在可變音量控制項中設定音量滑塊樣式的示例。

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```
