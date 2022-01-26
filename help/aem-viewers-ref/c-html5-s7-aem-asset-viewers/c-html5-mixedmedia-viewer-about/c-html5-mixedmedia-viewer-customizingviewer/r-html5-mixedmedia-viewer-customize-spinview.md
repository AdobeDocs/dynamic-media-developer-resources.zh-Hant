---
title: 旋轉視圖
description: 當當前資產為旋轉集時，主視圖由旋轉影像組成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 旋轉視圖{#spin-view}

當當前資產為旋轉集時，主視圖由旋轉影像組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

查看區域的外觀由以下CSS類選擇器控制：

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 旋轉視圖十六進位格式的背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使旋轉視圖透明。

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
