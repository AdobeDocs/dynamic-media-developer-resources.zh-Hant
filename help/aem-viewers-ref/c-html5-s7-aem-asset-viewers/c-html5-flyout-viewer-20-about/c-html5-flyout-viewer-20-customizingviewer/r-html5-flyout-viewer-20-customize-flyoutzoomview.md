---
title: 浮動縮放視圖
description: 主視圖由靜態影像和浮出視圖中顯示的縮放影像組成。 它還包括顯示在靜態影像上的高亮導航區域，以及顯示在靜態影像頂部的提示消息。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 2%

---

# 浮動縮放視圖{#flyout-zoom-view}

主視圖由靜態影像和浮出視圖中顯示的縮放影像組成。 它還包括顯示在靜態影像上的高亮導航區域，以及顯示在靜態影像頂部的提示消息。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在查看的影像的尺寸與浮動縮放視圖的尺寸不匹配，則影像內容將居中在浮動縮放視圖的矩形顯示區域中。

**主視圖的CSS屬性**

主視圖的外觀由以下CSS類選擇器控制：

```
.s7flyoutviewer .s7flyoutzoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 主視圖的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使主視圖透明：

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**彈出視圖的CSS屬性**

浮出視圖的外觀由以下CSS類選擇器控制：

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p> 浮出視圖相對於主視圖左上角的水準位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p> 出射視圖相對於主視圖左上角的垂直位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 浮出視圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>浮出視圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>浮出視圖的邊界。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 將浮出視圖設定為600 x 400像素，顯示時512 x 288主視圖右側偏移100像素：

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**主視圖中突出顯示的CSS屬性**

主視圖中突出顯示的外觀由以下CSS類選擇器控制：

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

可以使用CSS控制背景、邊框、透明度和類似屬性。 但是，高亮DOM元素的大小和位置由查看器邏輯管理。 不支援通過CSS覆蓋它。

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 高光的顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p> 突出顯示不透明度。 </p> <p>對於Internet Explorer 8，使用 <span class="codeph"> filter:alpha（不透明度 — ..）; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>邊框突出顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要設定具有40%透明度和一個像素紅色邊框的綠色高光：

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**游標的CSS屬性**

當 `highlightmode` 參數設定為 `cursor`，主視圖中的突出顯示將替換為固定大小的游標圖稿，該圖稿由CSS類選擇器控制：

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

可以使用CSS控制背景影像和大小。

適用的CSS屬性包括：

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p>游標圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>游標寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>游標高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>游標支援 `input` 屬性選擇器，可用於為不同設備應用不同的游標圖稿和大小。 特別是， `input="mouse"` 對應於案頭系統和 `input="touch"` 對應於觸摸設備。

**覆蓋的CSS屬性**

當 `overlay` 參數設定為 `1`，高光框或游標影像周圍的區域由CSS類選擇器控制：

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>覆蓋顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>覆蓋不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**提示消息的CSS屬性**

提示消息的外觀由以下CSS類選擇器控制：

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

可以通過CSS配置字型樣式、大小、外觀和垂直偏移。 但是，水準對齊由查看器邏輯管理。 使用 `left` 或 `right` 不支援屬性。

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從主視圖底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>文本顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列 </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小 </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>在消息文本週圍填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景填充顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊界半徑 </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景邊框半徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景不透明度。 </p> <p>對於Internet Explorer 8，使用 <span class="codeph"> filter:alpha（不透明度 — ..） </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

提示消息可以本地化。 請參閱 [用戶介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) 的子菜單。

示例 — 要設定半透明提示消息，其中帶有白色的Arial® 12-px字型，從主視圖底部偏移50個像素，填充和圓角邊框：

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
