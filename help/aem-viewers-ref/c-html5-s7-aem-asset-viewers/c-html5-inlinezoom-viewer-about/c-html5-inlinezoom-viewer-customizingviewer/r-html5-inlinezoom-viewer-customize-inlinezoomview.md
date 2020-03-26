---
description: 主視圖由靜態影像、在靜態影像上方的彈出視圖中顯示的縮放影像、以及在靜態影像上方顯示的提示資訊組成。
seo-description: 主視圖由靜態影像、在靜態影像上方的彈出視圖中顯示的縮放影像、以及在靜態影像上方顯示的提示資訊組成。
seo-title: 彈出式縮放檢視
solution: Experience Manager
title: 彈出式縮放檢視
topic: Dynamic media
uuid: a918c775-a36a-44e8-9ca4-90cb8f5c3a5e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Flyout zoom view{#flyout-zoom-view}

主視圖由靜態影像、在靜態影像上方的彈出視圖中顯示的縮放影像、以及在靜態影像上方顯示的提示資訊組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主視圖的CSS屬性**

主檢視的外觀是使用下列CSS類別選擇器來控制：

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

示例——使主視圖透明：

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**提示訊息的CSS屬性**

提示訊息的外觀是使用下列CSS類別選擇器來控制：

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

您可以透過CSS來設定字型樣式、大小外觀和垂直偏移。 不過，水準對齊方式是由檢視器邏輯管理。 不支援使用或 `left` 屬 `right` 性透過CSS覆寫它。

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
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
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
   <td colname="col2"> <p>訊息文字的背景填色顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框半徑 </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景邊框半徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>訊息文字的背景不透明度。 </p> <p>對於Internet Explorer 8，請 <span class="codeph"> 使用filter:alpha(opacity-...)) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

提示訊息可以本地化。 如需詳 [細資訊，請參閱使用者介面元素](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) 的本地化。

.

示例——要設定半透明的尖端消息，其中顯示白色的Arial 12像素字型、距主視圖底部50像素的偏移、填充和圓角邊框：

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

