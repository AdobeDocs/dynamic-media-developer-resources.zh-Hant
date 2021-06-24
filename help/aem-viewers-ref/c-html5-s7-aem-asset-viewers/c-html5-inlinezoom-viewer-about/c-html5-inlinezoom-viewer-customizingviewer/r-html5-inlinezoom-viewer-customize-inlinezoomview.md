---
description: 主視圖由靜態影像、在靜態影像頂部的彈出視圖中顯示的縮放影像以及在靜態影像頂部顯示的提示消息組成。
solution: Experience Manager
title: 彈出縮放視圖
feature: Dynamic Media Classic，檢視器，SDK/API，內嵌縮放
role: Developer,Business Practitioner
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 3%

---

# 彈出縮放視圖{#flyout-zoom-view}

主視圖由靜態影像、在靜態影像頂部的彈出視圖中顯示的縮放影像以及在靜態影像頂部顯示的提示消息組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視的CSS屬性**

主要檢視的外觀由下列CSS類別選取器控制：

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
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 主視圖的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要讓主檢視透明：

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**提示訊息的CSS屬性**

提示訊息的外觀由下列CSS類別選取器控制：

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

您可以透過CSS來設定字型樣式、大小外觀和垂直偏移。 不過，水準對齊方式是由檢視器邏輯管理。 不支援使用`left`或`right`屬性透過CSS覆寫它。

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
   <td colname="col2"> <p>文字色彩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p>在訊息文字周圍填補。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景填充顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框半徑  </span> </p> </td> 
   <td colname="col2"> <p>訊息文字的背景邊框半徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度  </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景不透明度。 </p> <p>對於Internet Explorer 8，請使用<span class="codeph"> filter:alpha(opacity-...))</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

提示訊息可本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) 。

.

示例 — 要設定半透明的尖端消息，其字型為白色Arial 12px，從主視圖底部偏移50像素，邊框間距和圓角：

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
