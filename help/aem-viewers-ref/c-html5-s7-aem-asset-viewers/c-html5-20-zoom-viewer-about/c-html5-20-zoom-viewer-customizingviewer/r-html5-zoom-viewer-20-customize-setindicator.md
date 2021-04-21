---
description: 設定指示器是當檢視器用於觸控裝置時，在色票上方呈現的一系列點。 當捲動按鈕無法使用時，這些點可協助使用者瀏覽縮圖頁面。
solution: Experience Manager
title: 設定指標
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 1%

---


# 設定指示符{#set-indicator}

設定指示器是當檢視器用於觸控裝置時，在色票上方呈現的一系列點。 當捲動按鈕無法使用時，這些點可協助使用者瀏覽縮圖頁面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**set指示符的CSS屬性**

使用下列CSS類別選擇器控制設定指標容器的外觀：

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
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>設定指示符的十六進位格式的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——要設定具有白色背景的設定指示符：

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

使用CSS類別選擇器控制個別設定指標點的外觀：

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
 </tbody> 
</table>

>[!NOTE]
>
>設定指標點支援`state`屬性選擇器，可用來將不同的外觀套用至不同的縮圖狀態。 尤其是，`state="selected"`對應於目前的縮圖頁面，`state="unselected"`對應於預設點狀態。

範例——若要將設定的指標點設定為15 x 15像素，具有兩個像素水準邊界、五個像素頂邊界、一個像素底邊界、十二個像素半徑、#D5D3D3預設顏色和#9393作用中顏色：

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

