---
title: 縮放檢視
description: 主檢視包含可縮放的影像。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 286b9df4-88db-4e5d-aab4-9cbe01195e57
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---

# 縮放檢視{#zoom-view}

主檢視包含可縮放的影像。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主要檢視器區域的&#x200B;**CSS屬性**

檢視區域的外觀是由下列CSS類別選取器所控制：

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p> 主檢視的十六進位格式的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">游標</span> </p> </td> 
   <td colname="col2"> <p>游標會顯示在主檢視上。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 讓主檢視透明。

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

在桌上型電腦系統上，元件支援`cursortype`屬性選取器（可套用至`.s7zoomview`類別），並根據元件狀態和使用者動作控制游標型別。 支援下列`cursortype`個值：

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">預設</span> </p> </td> 
   <td colname="col2"> <p>當影像因為影像解析度較小或元件設定（或兩者）而無法縮放時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>當影像可以放大時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">重設</span> </p> </td> 
   <td colname="col2"> <p>當影像處於最大縮放等級時顯示，並可重設為初始狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">拖曳</span> </p> </td> 
   <td colname="col2"> <p>當使用者平移處於放大狀態的影像時顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>
