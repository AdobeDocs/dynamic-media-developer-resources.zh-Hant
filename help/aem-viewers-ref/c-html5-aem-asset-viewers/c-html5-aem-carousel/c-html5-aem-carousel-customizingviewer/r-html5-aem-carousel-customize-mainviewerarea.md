---
title: 主查看器區域
description: 主視圖區域是旋轉木馬旗標影像所佔用的區域。 當未指定大小時，它設定為適合可用設備螢幕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: bdac54f5-79e3-4d3d-9c7e-d9a7cec61c73
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# 主查看器區域{#main-viewer-area}

主視圖區域是旋轉木馬旗標影像所佔用的區域。 當未指定大小時，它設定為適合可用設備螢幕。

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
   <td colname="col2"> <p>查看器的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>查看器的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 十六進位格式的背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定具有白色背景的查看器( `#FFFFFF`)，並使其尺寸為1174 x 500像素。

```
.s7carouselviewer { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```
