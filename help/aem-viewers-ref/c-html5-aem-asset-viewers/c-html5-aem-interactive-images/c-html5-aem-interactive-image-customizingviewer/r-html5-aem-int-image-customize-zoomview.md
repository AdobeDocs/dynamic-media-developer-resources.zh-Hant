---
description: 主視圖由靜態影像組成。
seo-description: 主視圖由靜態影像組成。
seo-title: 縮放檢視
solution: Experience Manager
title: 縮放檢視
uuid: d8349f8c-134f-4e74-9d0c-ab56981965d7
feature: Dynamic Media經典，檢視器，SDK/API，互動式影像
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---


# 縮放視圖{#zoom-view}

主視圖由靜態影像組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

檢視區域的外觀會使用下列CSS類別選擇器加以控制：

```
.s7interactiveimage .s7zoomview
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
   <td colname="col2"> <p> 主視圖的十六進位格式背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——使主視圖透明。

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```

