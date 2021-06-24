---
description: 設定指示器是在觸摸設備上使用查看器時在色板上呈現的一系列點。 當捲動按鈕無法使用時，點可協助使用者瀏覽縮圖的頁面。
solution: Experience Manager
title: 設定指示器
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,Business Practitioner
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---

# 設定指示器{#set-indicator}

設定指示器是在觸摸設備上使用查看器時在色板上呈現的一系列點。 當捲動按鈕無法使用時，點可協助使用者瀏覽縮圖的頁面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**設定指標的CSS屬性**

使用以下CSS類選擇器控制設定指示符容器的外觀：

```
.s7zoomviewer .s7setindicator
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

示例 — 要設定帶有白色背景的設定指示符：

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

使用CSS類選擇器控制單個設定指示符點的外觀：

`.s7zoomviewer .s7setindicator .s7dot`

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
 </tbody> 
</table>

>[!NOTE]
>
>設定指示符點支援`state`屬性選擇器，它可用於將不同的外觀應用於不同的縮略圖狀態。 特別是， `state="selected"`對應於縮略圖的當前頁， `state="unselected"`對應於預設點狀態。

範例：若要將指示器點設定為15 x 15像素，其中有兩個像素水準邊界、五個像素頂邊界、一個像素底邊界、十二個像素半徑、#D5D3D3預設顏色和#939393用顏色：

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
