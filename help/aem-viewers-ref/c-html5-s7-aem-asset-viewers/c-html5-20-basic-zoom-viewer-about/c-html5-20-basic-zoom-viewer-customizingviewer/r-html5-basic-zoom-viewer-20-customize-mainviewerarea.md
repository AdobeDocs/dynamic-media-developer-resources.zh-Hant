---
title: 主查看器區域
description: 主視圖區域是縮放影像所佔用的區域。 它通常設定為在未指定大小時適合可用設備螢幕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f51de2d6-0de2-4a4d-bbf4-185547e6c550
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# 主查看器區域{#main-viewer-area}

主視圖區域是縮放影像所佔用的區域。 它通常設定為在未指定大小時適合可用設備螢幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

查看區域的外觀由以下CSS類選擇器控制：

```
.s7basiczoomviewer
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

示例 — 設定具有白色背景的查看器( `#FFFFFF`)，使其尺寸為512 x 288像素。

```
.s7basiczoomviewer{ 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
