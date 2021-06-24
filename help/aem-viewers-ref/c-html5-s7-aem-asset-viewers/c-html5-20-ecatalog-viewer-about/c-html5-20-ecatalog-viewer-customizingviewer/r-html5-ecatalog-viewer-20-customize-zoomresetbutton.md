---
description: 按一下或點選此按鈕會重設主檢視中的影像。 此按鈕顯示在案頭系統和平板電腦的主控制欄中。 在行動電話上，此按鈕會顯示在影像的底部中央。 不過，影像處於重設狀態時不會顯示。 您可以使用CSS來調整此按鈕的大小、外觀和位置。
solution: Experience Manager
title: 縮放重設按鈕
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 6f0e22cd-12bd-4997-b874-539962504d3e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---

# 縮放重設按鈕{#zoom-reset-button}

按一下或點選此按鈕會重設主檢視中的影像。 此按鈕顯示在案頭系統和平板電腦的主控制欄中。 在行動電話上，此按鈕會顯示在影像的底部中央。 不過，影像處於重設狀態時不會顯示。 您可以使用CSS來調整此按鈕的大小、外觀和位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

按鈕的外觀由下列CSS類選擇器控制：

`.s7ecatalogviewer .s7zoomresetbutton`

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
   <td colname="col2"> <p>從主控制列（桌上型電腦和平板電腦）或檢視器（行動電話）的上邊框位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p>從主控制列（桌上型電腦和平板電腦）或檢視器（行動電話）的右邊框位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p>從主控制列（在桌上型電腦和平板電腦上）或檢視器（在行動電話上）的左側邊框位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從主控制列（在桌上型電腦和平板電腦上）或檢視器（在行動電話上）的底邊框位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

範例：若要設定28 x 28像素的縮放重設按鈕，從底部放置（案頭上）4像素，從主控制列的右邊放置47像素，並針對四個不同按鈕狀態中的每個顯示不同的影像。

```
.s7ecatalogviewer .s7zoomresetbutton { 
bottom:4px; 
right:47px; 
width:28px; 
height:28px; 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='up'] { 
background-image:url(images/v2/ZoomResetButton_dark_up.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='over'] {  
background-image:url(images/v2/ZoomResettButton_dark_over.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='down'] {  
background-image:url(images/v2/ZoomResetButton_dark_down.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='disabled'] { 
background-image:url(images/v2/ZoomResetButton_dark_disabled.png); 
}
```
