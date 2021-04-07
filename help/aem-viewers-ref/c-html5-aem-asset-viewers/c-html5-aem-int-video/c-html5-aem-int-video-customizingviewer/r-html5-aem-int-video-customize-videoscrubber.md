---
description: 視訊筆畫是水準滑桿控制項，可讓使用者動態尋找目前播放視訊中的任何時間位置。
solution: Experience Manager
title: 視訊筆刷
feature: Dynamic Media經典，檢視器，SDK/API，互動式視訊
role: 開發人員，商業從業人員
exl-id: 9d11f2e9-315c-44d8-beb1-530d2b316604
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 2%

---

# 視頻掃描器{#video-scrubber}

視訊筆畫是水準滑桿控制項，可讓使用者動態尋找目前播放視訊中的任何時間位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

當視訊播放時，Scrubber &#39;knob&#39;也會移動，以指出視訊在播放期間的目前時間位置。 視訊筆畫器一律會取得控制列的整個寬度。 您可將視訊筆畫變成外觀。 使用CSS來變更其高度和垂直位置。

使用下列CSS類別選擇器控制視訊筆畫的一般外觀：

```
.s7interactivevideoviewer .s7videoscrubber 
.s7interactivevideoviewer .s7videoscrubber .s7videotime 
.s7interactivevideoviewer .s7videoscrubber .s7knob
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
.s7interactivevideoviewer .s7videoscrubber .s7track 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed
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
.s7interactivevideoviewer .s7videoscrubber .s7knob
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
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

下列CSS類別選擇器控制播放的泡泡時間：

```
.s7interactivevideoviewer .s7videoscrubber .s7videotime
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
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>文字與泡泡區域對齊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

視訊筆畫工具提示可以局部化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

**範例** -若要設定視訊檢視器，使用自訂軌道色彩（高度為10像素）來設定視訊檢視器，並從控制列的上邊緣和左邊緣放置10像素和35像素。

```
.s7interactivevideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

當使用`navigation`參數啟用視訊分頁時，分頁位置會顯示為視訊筆畫軌道上方的標籤。

視訊章節標籤由下列CSS類別選擇器控制：

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation
```

**視訊章節標籤的CSS屬性**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節標籤寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節標籤高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節標籤圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，您可使用它將不同的外觀套用至不同的按鈕狀態。 尤其是，`selected='default'`對應於預設的視訊章節標籤狀態，當視訊章節標籤由滑鼠置於或觸控手勢啟動時，會使用`selected='over'`。

**範例** -若要設定視訊章節標籤，此標籤為5 x 8像素，並針對「預設」和「over」狀態使用不同的圖稿。

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

視訊章節泡泡位於視訊章節標籤的上方，並顯示特定章節的標題、開始時間和說明。 可以控制相對於視頻掃描器軌道的最大氣泡寬度和垂直偏移。 其餘部分由元件自動計算。

視訊章節泡泡是由下列CSS類別選擇器控制：

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter
```

**視訊章節泡泡的CSS屬性**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 最大寬度  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節氣泡的最大寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>與視訊Scrubber軌道垂直偏移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例** -若要設定視訊章節泡泡，該泡泡寬235像素，且距視訊筆畫軌道底部上方8像素。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

視訊章節泡泡由選用的標題和內容組成。 頁首具有可選的章節開始時間和章節標題。

標題由下列CSS類別選擇器控制：

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header
```

**視訊章節氣泡標題的CSS屬性**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節氣泡標題高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>視訊章節氣泡標題文字的內部填補。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節氣泡標題背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 線高  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節氣泡標題文字行高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例** -若要設定高22像素、高22像素、12像素水準邊界和灰色背景的視訊章節泡泡標題。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

視訊章節的開始時間由下列CSS類別選擇器控制：

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**視訊章節開始時間的CSS屬性**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顏色  </span> </p> </td> 
   <td colname="col2"> <p>文字色彩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p>字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右邊填充  </span> </p> </td> 
   <td colname="col2"> <p> 開始時間和章節標題之間的間距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例** -若要使用灰色十像素Verdana字型設定章節開始時間，並在右側填入十像素。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

視訊章節標題由下列CSS類別選擇器控制：

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**視訊章節標題的CSS屬性**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顏色  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節標題文字顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p>影片章節標題字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節標題字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>影片章節標題字型系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例** -若要設定使用白色、粗體、十像素Verdana字型的影片章節標題。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

視訊章節說明由下列CSS類別選擇器控制：

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description
```

**視訊章節說明的CSS屬性**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顏色  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節說明文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節說明背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節說明字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節說明字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節說明字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 線高  </span> </p> </td> 
   <td colname="col2"> <p>視訊章節描述行高。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>視訊章節說明內部填補。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例** -使用深灰色、11像素的Verdana字型，以淺灰色背景設定視訊章節描述；5像素行高、12像素水準間距、12像素頂部間距和9像素底部間距。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

章節氣泡底部的楔形連接器由下列CSS類別選擇器控制：

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail
```

**楔形連接器的CSS屬性**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框色彩  </span> </p> </td> 
   <td colname="col2"> <p>楔形接頭顏色。 </p> <p>定義為<span class="codeph"> &lt;color&gt;透明</span>，因此僅定義頂部邊框顏色，而其餘邊框保持透明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框寬度  </span> </p> </td> 
   <td colname="col2"> <p> 楔形連接器寬度。 </p> <p>定義為<span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span>，以便僅為頂部和水準邊界定義相同寬度，並且底部邊框寬度為<span class="codeph"> 0 </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 僅定義負底邊距。 其值應與<span class="codeph"> border-width </span>的值相同。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例** -要設定灰色、六像素楔形連接器：

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
