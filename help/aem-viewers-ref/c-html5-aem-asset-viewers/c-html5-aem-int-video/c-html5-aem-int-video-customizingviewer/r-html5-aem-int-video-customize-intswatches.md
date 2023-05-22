---
title: 互動式色板
description: 如果交互資料在配置中傳遞到查看器，則互動式色板面板會出現在視頻內容旁邊。 它由頂部的標題組成，該標題可呈現文本，如「按一下查看」、包含一個或多個互動式色板的列以及兩個滾動按鈕（僅在案頭系統上可用）。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 2%

---

# 互動式色板{#interactive-swatches}

如果交互資料在配置中傳遞到查看器，則互動式色板面板會出現在視頻內容旁邊。 它由頂部的標題組成，該標題可呈現文本，如「按一下查看」、包含一個或多個互動式色板的列以及兩個滾動按鈕（僅在案頭系統上可用）。

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

在案頭系統和觸摸設備上，以橫向方向，互動式色板垂直呈現在視頻內容的右側。 在縱向方向的觸摸設備上，它們以水準色板行的形式顯示在查看器底部。

以下CSS類選擇器控制交互色板面板的位置和方向：

```
.s7interactivevideoviewer .s7interactiveswatches
```

## 交互色板的CSS屬性 {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>互動式色板面板的寬度 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>互動式色板面板的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>互動式色板面板的頂部位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>交互色板面板的底部位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p>互動式色板面板的左側位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p>互動式色板面板的右側位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

互動式色板面板的運行時位置和方向由上述CSS屬性的組合定義，如下所示：

* 要在查看器底部水準呈現互動式色板，請將高度設定為絕對像素值；從左到下到0px;寬度，右，上到自動。
* 要垂直於視頻內容的右側呈現互動式色板，請將寬度設定為絕對像素；右上至0px;高度，從左到下到自動。

可以將此樣式使用CSS標籤來實現互動式色板面板的自適應放置。

## 範例 {#example}

設定互動式色板面板，以在觸摸設備上以橫向方向在查看器底部水準呈現。 而且，在所有其他情況下，要垂直顯示視頻內容的右側：

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

橫幅的大小和位置由交互色板元件根據與CSS一起應用的其它樣式進行管理，無法顯式設定。

以下CSS類選擇器控制標題面板的外觀：

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## 標題面板的CSS屬性 {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>標題面板內的文本顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型粗細 </span> </p> </td> 
   <td colname="col2"> <p>用於橫幅面板內文本的字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小 </span> </p> </td> 
   <td colname="col2"> <p>用於橫幅面板內文本的字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列 </span> </p> </td> 
   <td colname="col2"> <p>用於橫幅面板內文本的字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型對齊 </span> </p> </td> 
   <td colname="col2"> <p>用於橫幅面板內文本的字型對齊方式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以對橫幅工具提示進行本地化。 請參閱 [用戶介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 的子菜單。

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

要設定帶有深灰色背景、淺灰色雙像素邊框和水準居中白色文本的橫幅：

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
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>色板區域的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-9cadd62a09fd44a280f55ff42437e416}

要設定具有深灰色背景的色板區域：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

以下CSS類選擇器控制色板縮略圖之間的間距：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## 色板縮略圖間距的CSS屬性 {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每個縮覽圖周圍的水準和垂直邊距的大小。 實際縮略圖間距等於為設定的左邊距和右邊距的和 <span class="codeph"> .s7拇指單元 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-39fb270b7e494a9d99e6e8f6890ec53c}

要將垂直間距設定為十像素：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

以下CSS類選擇器控制各個縮略圖的外觀：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## 單個縮略圖外觀的CSS屬性 {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮略圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮略圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>縮略圖的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮略圖支援 `state` 屬性選擇器，您可以使用它將不同的外觀應用到不同的縮略圖狀態。 特別是， `state="selected"` 與當前選定影像的縮略圖對應； `state="default"` 與其餘縮略圖對應； `state="over"` 用於滑鼠懸停。

## 範例 {#section-69fec189ffaa440b97b6b846c320b75b}

設定100 x 75像素的縮略圖：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

以下CSS類選擇器控制縮略表徵圖簽的外觀：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## 縮略表徵圖簽外觀的CSS屬性 {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>文本顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>標籤邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 文本對齊 </span> </p> </td> 
   <td colname="col2"> <p>水準文本對齊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列 </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-eb141eb6c1154183baa69796edb90536}

要設定標籤，以左對齊、白色、12像素、Helvetica®字型和下邊框：

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

無法使用CSS定位滾動按鈕 `top`。 `left`。 `bottom`, `right` 屬性；相反，查看器邏輯自動定位它們。

## 上下滾動按鈕外觀的CSS屬性 {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>滾動按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>滾動按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p>為給定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p>使用CSS浮雕時，圖稿浮雕內的位置。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS繁體 </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，您可以使用它將不同的外觀應用於按鈕狀態：&quot; `up`&quot;, &quot; `down`&quot;, &quot; `over`&quot;和&quot; `disabled`。

按鈕工具提示可以本地化。 請參閱 [用戶介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 的子菜單。

## 範例 {#section-e6ce4fa084b84288bc7583342b2c510c}

要設定60 x 36像素的向上滾動按鈕，請針對每種狀態設定不同的圖稿，並從元件的sprite影像中獲取該圖稿：

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
