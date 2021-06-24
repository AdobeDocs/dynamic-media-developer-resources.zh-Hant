---
description: 主視圖由靜態影像、彈出視圖中顯示的縮放影像、靜態影像上顯示的突出顯示導航區域以及靜態影像上顯示的提示消息組成。
solution: Experience Manager
title: 彈出縮放視圖
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 3%

---

# 彈出縮放視圖{#flyout-zoom-view}

主視圖由靜態影像、彈出視圖中顯示的縮放影像、靜態影像上顯示的突出顯示導航區域以及靜態影像上顯示的提示消息組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果所查看影像的尺寸與彈出縮放視圖的尺寸不匹配，則影像內容會置於彈出縮放視圖的矩形顯示區域中。

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

**飛出檢視的CSS屬性**

飛出檢視的外觀由下列CSS類別選取器控制：

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
   <td colname="col2"> <p> 彈出視圖相對於主視圖左上角的水準位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p> 彈出視圖相對於主視圖左上角的垂直位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 彈出視圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>彈出視圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>彈出視圖的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將彈出檢視設為600 x 400像素，以100像素的位移顯示，而512 x 288主檢視的右側有上一個範例所示：

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

您可以使用CSS控制背景、邊框、透明度和類似屬性。 不過，反白顯示DOM元素的大小和位置由檢視器邏輯管理。 不支援透過CSS覆寫它。

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 突出顯示的顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度  </span> </p> </td> 
   <td colname="col2"> <p> 突出顯示不透明度。 </p> <p>對於Internet Explorer 8，請使用<span class="codeph"> filter:alpha(opacity-...));</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框  </span> </p> </td> 
   <td colname="col2"> <p>邊框醒目提示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定透明度為40%的綠色高亮和一個像素紅色邊框：

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**游標的CSS屬性**

當`highlightmode`參數設定為`cursor`時，主視圖中的突出顯示將替換為固定大小的游標圖稿，該圖稿由CSS類選擇器控制：

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

您可以使用CSS控制背景影像和大小。

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
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>游標插圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>游標寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>游標高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>游標支援`input`屬性選擇器，它可用於為不同設備應用不同的游標圖稿和大小。 具體來說，`input="mouse"`對應於案頭系統，`input="touch"`對應於觸摸設備。

**覆蓋的CSS屬性**

當`overlay`參數設定為`1`時，高亮幀或游標影像周圍的區域由CSS類選擇器控制：

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
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>覆蓋顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度  </span> </p> </td> 
   <td colname="col2"> <p>覆蓋不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

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

提示訊息可本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) 。

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
