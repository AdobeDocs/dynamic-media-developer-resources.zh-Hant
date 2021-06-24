---
description: 如果在設定中將互動式資料傳遞至檢視器，則互動式色票面板會出現在視訊內容旁。 它由頂端的橫幅組成，可呈現「按一下即可檢視」等文字、一欄或多個互動色票和兩個捲動按鈕（僅適用於案頭系統）。
solution: Experience Manager
title: 互動色票
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 2%

---

# 互動色票{#interactive-swatches}

如果在設定中將互動式資料傳遞至檢視器，則互動式色票面板會出現在視訊內容旁。 它由頂端的橫幅組成，可呈現「按一下即可檢視」等文字、一欄或多個互動色票和兩個捲動按鈕（僅適用於案頭系統）。

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

在案頭系統和觸控裝置上，以橫向方向，互動式色票會垂直轉譯至視訊內容的右側。 在縱向的觸控裝置上，它們會以水準色票列的形式顯示在檢視器底部。

以下CSS類選擇器控制交互色板面板的位置和方向：

```
.s7interactivevideoviewer .s7interactiveswatches
```

## 互動色票的CSS屬性 {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>互動色板面板的寬度 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>互動色票面板的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>互動色票面板的頂端位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>交互色板面板的底部位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p>交互色板面板的左側位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p>交互色板面板的右側位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

互動式色票面板的執行時間位置和方向由上述CSS屬性的組合定義，如下所示：

* 要在查看器底部水準渲染交互色板，請將高度設定為絕對像素值；從左到下到0px;寬度、右和上到自動。
* 若要垂直地向視頻內容的右側呈現互動色板，請將寬度設定為絕對像素；右上至0px;高度，左下角自動。

您可以結合此樣式使用CSS標籤，以實現互動式色票面板的最適化放置。

## 範例 {#example}

若要設定互動式色票面板，以便在觸控裝置上以橫向方向在檢視器底部水準轉譯，並在所有其他情況下以垂直向右顯示視訊內容：

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

橫幅的大小和位置是由互動式色票元件根據套用至CSS的其他樣式來管理，且無法明確設定。

以下CSS類選擇器控制橫幅面板的外觀：

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## 橫幅面板的CSS屬性 {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板內的文字顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細  </span> </p> </td> 
   <td colname="col2"> <p>用於橫幅面板內文字的字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>用於橫幅面板內文本的字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>用於橫幅面板內文本的字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>用於橫幅面板內文本的字型對齊方式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

橫幅工具提示可本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

要設定帶有深灰色背景、較淺灰色的兩個像素邊框以及水準居中的白文本的橫幅：

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

以下CSS類選擇器控制色板的外觀：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## 色板區域的CSS屬性 {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>色板區域的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-9cadd62a09fd44a280f55ff42437e416}

要設定帶有深灰色背景的色板區域：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

以下CSS類選擇器控制色板縮略圖之間的間距：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## 色板的CSS屬性縮略圖間距 {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖周圍的水準和垂直邊界的大小。 實際縮圖間距等於為<span class="codeph"> .s7thumbcell </span>設定的左邊距和右邊距的總和。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-39fb270b7e494a9d99e6e8f6890ec53c}

若要將垂直間距設定為10像素：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

以下CSS類選擇器控制各個縮略圖的外觀：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## 個別縮圖外觀的CSS屬性 {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>縮圖寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>縮圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框  </span> </p> </td> 
   <td colname="col2"> <p>縮圖的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援`state`屬性選取器，您可使用它將不同的外觀套用至不同的縮圖狀態。 尤其`state="selected"`對應於目前所選影像的縮圖；`state="default"`對應至其餘縮圖；`state="over"`用於滑鼠暫留。

## 範例 {#section-69fec189ffaa440b97b6b846c320b75b}

設定縮圖100 x 75像素：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

以下CSS類選擇器控制縮略表徵圖簽的外觀：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## 縮表徵圖簽外觀的CSS屬性 {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 色彩  </span> </p> </td> 
   <td colname="col2"> <p>文字色彩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框  </span> </p> </td> 
   <td colname="col2"> <p>標籤邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 文本對齊  </span> </p> </td> 
   <td colname="col2"> <p>水準文字對齊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-eb141eb6c1154183baa69796edb90536}

要設定標籤，使用左對齊、白色、12像素、Helvetica字型和底邊框：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

以下CSS類選擇器控制上下滾動按鈕的外觀：

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

無法使用CSS `top`、`left`、`bottom`和`right`屬性來定位捲動按鈕；反之，檢視器邏輯會自動定位。

## 上下捲動按鈕外觀的CSS屬性 {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>捲動按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>捲動按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p>使用CSS精靈的圖稿精靈內的位置。 </p> <p>另請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，您可使用它將不同的外觀應用於按鈕狀態：&quot; `up`&quot;、&quot; `down`&quot;、&quot; `over`&quot;和&quot; `disabled`&quot;。

按鈕工具提示可翻譯。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

## 範例 {#section-e6ce4fa084b84288bc7583342b2c510c}

要設定60 x 36像素的向上滾動按鈕，請為每個狀態具有不同的圖稿，並從元件的Sprite影像中獲取該圖稿：

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```
