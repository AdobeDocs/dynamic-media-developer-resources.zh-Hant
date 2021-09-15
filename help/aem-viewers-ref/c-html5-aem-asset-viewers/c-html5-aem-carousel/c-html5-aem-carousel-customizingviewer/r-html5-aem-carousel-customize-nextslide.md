---
title: 下一張幻燈片
description: 選取「下一張」(Next)幻燈片按鈕，可將使用者移至轉盤集中的下一張幻燈片。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: c64889bb-bcbe-49c6-a0be-b4013ead7b90
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 3%

---

# 下一張幻燈片{#next-slide}

選取「下一張」(Next)幻燈片按鈕，可將使用者移至轉盤集中的下一張幻燈片。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

觸控裝置上不會顯示此按鈕。 您可以使用CSS來調整此按鈕的大小、外觀和位置。

**主查看器區域的CSS屬性**

按鈕的外觀由下列CSS類選擇器控制：

`.s7carouselviewer .s7panrightbutton`

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
   <td colname="col2"> <p>從檢視器邊框的頂端位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p>從檢視器邊框的右側放置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p>檢視器左側的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從檢視器邊框的底部位置。 </p> </td> 
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
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS空格</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 游標  </span> </p> </td> 
   <td colname="col2"> <p>游標類型。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md) 。

例如，假設您要設定一個上一個幻燈片按鈕，即60 x 60像素。 您希望按鈕從右側檢視器邊框放置十個像素，並垂直居中。 而且，您希望它針對四個不同的按鈕狀態顯示不同的影像。

```
.s7carouselviewer .s7panrightbutton{ 
 bottom: 50%; 
 right: 10px; 
 background-size:60px; 
 cursor: pointer; 
 } 
.s7carouselviewer.s7mouseinput .s7panrightbutton { 
 width:60px; 
 height:60px; 
 margin-bottom: -20px; 
} 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state]  { 
    background-image: url(../../viewers/s7viewers/html5/images/v2/CarouselDotsRightButton_dark_sprite.png); 
} 
 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='up'] { background-position: -0px -60px;  } 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='over'] { background-position: -0px -0px; } 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='down'] { background-position: -0px -0px; } 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='disabled'] { background-position: -0px -60px; }
```
