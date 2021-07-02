---
description: 當目前資產為回轉集時，主檢視由回轉影像組成。
solution: Experience Manager
title: 回轉檢視
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,Business Practitioner
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# 回轉檢視{#spin-view}

當目前資產為回轉集時，主檢視由回轉影像組成。

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
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 以十六進位格式表示的回轉視圖背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：讓回轉檢視透明。

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
