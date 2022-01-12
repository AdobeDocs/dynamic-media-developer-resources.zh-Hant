---
title: 調色板
description: 色票由一列縮圖影像組成，左側和右側有可選的捲動按鈕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: bd385b06-b8d6-4c6e-83fd-65a3d1c105c5
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 3%

---

# 調色板{#swatches}

色票由一列縮圖影像組成，左側和右側有可選的捲動按鈕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

只有當所有縮圖都無法放入容器寬度時，捲動按鈕才會顯示在案頭上。 在行動裝置上，或如果縮圖可符合容器寬度，則不會顯示捲動按鈕。

**色票的CSS屬性**

使用以下CSS類選擇器控制色板容器的外觀：

```
.s7flyoutviewer .s7swatches
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 色票的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>色票的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 垂直色票相對於檢視器容器偏移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要將色票設定為460 x 100像素：

```
.s7flyoutviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

**縮圖色票間距的CSS屬性**

使用CSS類選擇器控制色板縮圖之間的間距：

```
.s7flyoutviewer .s7swatches .s7thumbcell
```

<table id="table_70FAD50E38EB4647B8FAB832F552BBB8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖周圍的水準和垂直邊界的大小。 實際縮圖間距等於設定的左右邊界總和 <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要將間距設定為垂直和水準10個像素：

```
.s7flyoutviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

**縮圖色票的CSS屬性**

個別縮圖的外觀由下列CSS類別選取器控制：

```
.s7flyoutviewer .s7swatches .s7thumb
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
   <td colname="col1"> <p> <span class="codeph"> 寬度 </span> </p> </td> 
   <td colname="col2"> <p> 縮圖色票的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p>縮圖色票的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>縮圖色票的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援 `state` 屬性選取器，用於將不同的外觀套用至不同的縮圖狀態。 特別是， `state="selected"` 對應於當前顯示在主視圖中的影像的縮略圖， `state="default"` 與縮圖的其餘部分對應， `state="over"` 用於滑鼠暫留。

範例 — 若要設定縮圖，縮圖為56 x 56像素、有淺灰色預設邊框和深灰色選取的邊框：

```
.s7flyoutviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7flyoutviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7flyoutviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

**左右捲動按鈕的CSS屬性**

左和右捲動按鈕的外觀由下列CSS類選擇器控制：

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton 
.s7flyoutviewer .s7swatches .s7scrollrightbutton
```

無法使用CSS定位捲動按鈕 `top`, `left`, `bottom`，和 `right` 屬性。 檢視器邏輯會自動定位。

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度 </span> </p> </td> 
   <td colname="col2"> <p> 捲動按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p>捲動按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像 </span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#section-b0af39db1af74561aea9fddcc8cdc2c7" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選取器，用於將不同外觀套用至按鈕狀態 `up`, `down`, `over`，和 `disabled`.

按鈕工具提示可翻譯。 請參閱 [用戶介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) 以取得更多資訊。

示例 — 要設定56 x 56像素的捲動按鈕，並且每個狀態的圖稿都不同：

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```
