---
description: 設定指標是在檢視器底部轉譯的一系列點。 它顯示集內的當前位置。
solution: Experience Manager
title: 設定指示器
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,Business Practitioner
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# 設定指示器{#set-indicator}

設定指標是在檢視器底部轉譯的一系列點。 它顯示集內的當前位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**設定指標的CSS屬性**

使用以下CSS類選擇器控制設定指示符容器的外觀：

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
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>設定指示器的十六進位格式的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>設定指示器支援模式屬性選擇器，可用於為虛線和數字操作模式應用不同的樣式。 具體來說，`mode="numeric"`對應於數字操作模式；`mode="dotted"`對應於預設點狀態。

示例 — 要設定帶有白色背景的設定指示符：

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

使用CSS類選擇器控制單個設定指示符點的外觀。 它適用於點分和數值操作模式中的項目。

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
   <td colname="col2"> <p>設定指示點的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>設定指示器點的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊距  </span> </p> </td> 
   <td colname="col2"> <p>左邊距（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距上  </span> </p> </td> 
   <td colname="col2"> <p>上邊界（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距 — 右  </span> </p> </td> 
   <td colname="col2"> <p>右邊距（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距 — 底部  </span> </p> </td> 
   <td colname="col2"> <p>底邊界（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框半徑  </span> </p> </td> 
   <td colname="col2"> <p>邊框半徑（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>以十六進位格式表示的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
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
>設定指標項目支援`state`屬性選擇器，可用於將不同的外觀應用於不同的縮略圖狀態。 具體而言，`state="selected"`對應於集合中的當前元素；`state="unselected"`對應至預設項目狀態。

示例 — 以虛線模式設定指示器，以便案頭系統從查看器底部放置20像素。 未選取的點為黑色，具有50%的透明度，15 x 15像素，具有7個像素的圓角。 所選點為黑色，透明度為90%,18 x 18像素，圓角為9像素。 點之間的間距為5像素。

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
