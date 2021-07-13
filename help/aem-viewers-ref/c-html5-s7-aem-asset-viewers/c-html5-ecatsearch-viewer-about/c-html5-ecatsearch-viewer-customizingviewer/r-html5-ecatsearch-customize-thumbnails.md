---
description: 縮圖由縮圖影像的格線組成，右側可選用捲軸，以允許垂直捲動。
solution: Experience Manager
title: 縮圖
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,User
exl-id: 25032917-237c-4227-92bd-ce66a6d003a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 2%

---

# 縮圖{#thumbnails}

縮圖由縮圖影像的格線組成，右側可選用捲軸，以允許垂直捲動。

按一下主控制列中的縮圖按鈕來切換縮圖。 當縮圖作用中時，會以重疊在檢視器使用者介面上方的強制回應模式顯示。 檢視器邏輯會自動將縮圖容器調整為整個檢視器區域的大小。

縮圖容器的外觀由下列CSS類選擇器控制：

`.s7ecatalogsearchviewer .s7thumbnailgridview`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p> 縮圖容器從檢視器頂端的垂直偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距上  </span> </p> </td> 
   <td colname="col2"> <p>最大利潤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊距  </span> </p> </td> 
   <td colname="col2"> <p>左邊距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距 — 右  </span> </p> </td> 
   <td colname="col2"> <p>右邊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距 — 底部  </span> </p> </td> 
   <td colname="col2"> <p>底邊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>縮圖區域的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定縮圖，使其從上方偏移32像素，左右邊距為5像素，底部邊距為8像素，背景為`0xDDDDDD`。

```
.s7ecatalogsearchviewer .s7thumbnailgridview { 
 top: 32px; 
 margin-left: 5px; 
 margin-right: 5px; 
 margin-bottom: 8px; 
 background-color: rgb(221, 221, 221); 
}
```

縮圖之間的間距由下列CSS類選擇器控制：

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumbcell`

<table id="table_1D93AB60E57F49A8838EA825CD6B7897"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖周圍的水準和垂直邊界的大小。 實際水準縮圖間距等於為<span class="codeph"> .s7thumbcell </span>設定的左邊距和右邊距之和。 垂直縮圖間距等於上邊界和下邊界的總和。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：垂直和水準設定10個像素空間。

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumbcell { 
 margin: 5px; 
}
```

個別縮圖的外觀由下列CSS類別選取器控制：

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb`

<table id="table_1D973EA6C36947F092AAA16CFE9B44A1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>縮圖的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>縮圖的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

在觸控裝置上，當旋轉為縱向模式時，檢視器可能會將縮圖大小為所設定內容的一半，以備決定將目錄跨頁分割為個別頁面時使用。

>[!NOTE]
>
>縮圖支援`state`屬性選取器，可用來將不同外觀套用至不同的縮圖狀態。 尤其是， `state="selected"`對應於當前顯示在主視圖中的影像的縮略圖， `state="default"`對應於其餘的縮略圖，並且`state="over"`用於滑鼠懸停。

範例 — 若要設定縮圖，縮圖為120 x 85像素、有白色背景、淺灰色標準邊框和深灰色選取的邊框。

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb { 
 width:120px; 
 height:85px; 
 background-color: rgb(255, 255, 255); 
 border: solid 1px #999999; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb[state="selected"]{ 
 border: solid 2px #666666; 
}
```

縮表徵圖簽的外觀由下列CSS類選擇器控制：

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7label`

<table id="table_E242176042F247F8B51A0D5ADB645E20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 將標籤設定為使用14像素Helvetica字型。

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 12px; 
}
```

如果縮圖數量超過垂直放入檢視的大小，縮圖會在右側呈現垂直捲軸。 使用以下CSS類選擇器控制捲動條區域的外觀：

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar`

<table id="table_F05EC87CD9A946DB9B4B2B48E0784168"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>捲動條的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p> 垂直捲動條從縮圖區域的頂部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>垂直捲動條從縮圖區域底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p> 水準捲動條從縮圖區域的右邊緣偏移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：設定寬28像素的捲軸，並從縮圖區域的上、右和下方有8像素邊距。

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar { 
 top:8px; 
 bottom:8px; 
 right:8px; 
 width:28px; 
}
```

捲動條軌跡是頂部和底部捲動按鈕之間的區域。 元件會自動設定軌跡的位置和高度。 使用下列CSS類別選取器控制追蹤：

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack`

<table id="table_EF1B91F9E984451EB0AB48175D917726"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>捲動條軌道的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 捲動條軌道的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定寬28像素且半透明灰色背景的捲軸軌道。

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

捲動條拇指在捲動軌道區域內垂直移動。 其垂直位置完全由元件邏輯控制，但縮圖高度不會根據內容量而動態改變。 縮圖高度和其他方面由下列CSS類選擇器控制：

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb`

<table id="table_5C791F6E90E64E7A9F1DB7C9B2FDC528"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>捲動條拇指的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>捲動條縮圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框間距 — 頂端  </span> </p> </td> 
   <td colname="col2"> <p>捲動條軌道頂部之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框間距  </span> </p> </td> 
   <td colname="col2"> <p>捲動條軌道底部之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>為給定拇指狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb支援`state`屬性選擇器，該選擇器可用於將不同的外觀應用於Thumb狀態`up`、`down`、`over`和`disabled`。

示例 — 要設定一個捲動條縮圖，該縮圖為28 x 45像素，頂部和底部有10個像素邊距，並且每個狀態的圖稿都不同。

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

使用以下CSS類選擇器控制頂部和底部捲動按鈕的外觀：

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton`

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton`

無法使用CSS `top`、`left`、`bottom`和`right`屬性來定位捲動按鈕。 檢視器邏輯會自動定位。

<table id="table_89E64A138ABF463F9650BB454F22D530"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>為給定拇指狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>這些按鈕支援`state`屬性選擇器，可用於將不同外觀應用於不同的按鈕狀態`up`、`down`、`over`和`disabled`。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例 — 設定捲動按鈕，這些按鈕為28 x 32像素，並且每個狀態的圖稿都不同。

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
