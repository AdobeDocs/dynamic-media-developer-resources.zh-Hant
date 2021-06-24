---
description: 主要檢視區域是轉盤橫幅影像所佔用的區域。 當未指定大小時，通常會設定為適合可用的裝置畫面。
solution: Experience Manager
title: 主觀看者區域
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,Business Practitioner
exl-id: bdac54f5-79e3-4d3d-9c7e-d9a7cec61c73
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 2%

---

# 主觀看者區域{#main-viewer-area}

主要檢視區域是轉盤橫幅影像所佔用的區域。 當未指定大小時，通常會設定為適合可用的裝置畫面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

查看區域的外觀由以下CSS類選擇器控制：

```
.s7carouselviewer
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
   <td colname="col2"> <p>檢視器的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>檢視器的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 以十六進位格式表示的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要設定具有白色背景的檢視器(`#FFFFFF`)，並將其大小設為1174 x 500像素。

```
.s7carouselviewer { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```
