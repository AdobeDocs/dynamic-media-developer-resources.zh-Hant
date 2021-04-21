---
description: 設定指標是檢視器底部呈現的一系列點。 它顯示集內的當前位置。
solution: Experience Manager
title: 設定指標
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---

# 設定指示符{#set-indicator}

設定指標是檢視器底部呈現的一系列點。 它顯示集內的當前位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**set指示符的CSS屬性**

使用下列CSS類別選擇器控制設定指標容器的外觀：

```
.s7carouselviewer .s7setindicator
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
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>設定指示符的十六進位格式的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>設定指示符支援模式屬性選擇器，可用於為虛線和數字操作模式應用不同的樣式。 具體來說，`mode="numeric"`對應於數字操作模式；`mode="dotted"`對應於預設點狀態。

示例——要設定具有白色背景的設定指示符：

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

使用CSS類別選擇器控制個別設定指標點的外觀。 它適用於點狀和數字操作模式中的項目。

`.s7carouselviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>設定指示器點的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>設定指示點的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊距  </span> </p> </td> 
   <td colname="col2"> <p>左邊界（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距頂端  </span> </p> </td> 
   <td colname="col2"> <p>上邊界（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊界右側  </span> </p> </td> 
   <td colname="col2"> <p>右邊距（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距——底部  </span> </p> </td> 
   <td colname="col2"> <p>底部邊界（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框半徑  </span> </p> </td> 
   <td colname="col2"> <p>邊框半徑（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>十六進位格式的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>字型顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 垂直對齊  </span> </p> </td> 
   <td colname="col2"> <p>橫幅索引的垂直對齊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 線高  </span> </p> </td> 
   <td colname="col2"> <p>橫幅索引的文字高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>設定指標項目支援`state`屬性選擇器，可用來將不同的外觀套用至不同的縮圖狀態。 特別是`state="selected"`對應於集合中的當前元素；`state="unselected"`對應於預設項目狀態。

範例——以點狀模式設定指示符，讓案頭系統從檢視器底部放置20像素。 未選取的點是黑色，具有50%的透明度，15 x 15像素，7像素為圓角。 選取的點是黑色，具有90%的透明度、18 x 18像素和9像素的圓角。 點之間的間距為5像素。

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```
