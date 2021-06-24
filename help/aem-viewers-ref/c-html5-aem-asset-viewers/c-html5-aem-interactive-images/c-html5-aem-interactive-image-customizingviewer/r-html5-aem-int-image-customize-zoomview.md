---
description: 主檢視包含靜態影像。
solution: Experience Manager
title: 縮放檢視
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影像
role: Developer,Business Practitioner
exl-id: e83d53a1-bee9-4e4d-8295-a3a350f3ff9c
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---

# 縮放檢視{#zoom-view}

主檢視包含靜態影像。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

查看區域的外觀由以下CSS類選擇器控制：

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
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 主視圖的十六進位格式背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使主視圖透明。

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```
