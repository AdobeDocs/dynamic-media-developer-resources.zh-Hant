---
description: 主檢視包含可縮放的影像。
seo-description: 主檢視包含可縮放的影像。
seo-title: 縮放檢視
solution: Experience Manager
title: 縮放檢視
topic: Dynamic media
uuid: 06464e36-8c9c-4d3c-b4e5-5911f002568c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 縮放視圖{#zoom-view}

主檢視包含可縮放的影像。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

檢視區域的外觀會使用下列CSS類別選擇器加以控制：

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
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p> 主視圖的十六進位格式背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 游標  </span> </p> </td> 
   <td colname="col2"> <p>游標顯示在主視圖上。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——使主視圖透明。

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

在案頭系統上，元件支援`cursortype`屬性選擇器，該選擇器可應用於`.s7zoomview`類，並根據元件狀態和用戶操作控制游標類型。 支援下列`cursortype`值：

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p>當影像因影像解析度小或元件設定或兩者皆無法縮放時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 牛  </span> </p> </td> 
   <td colname="col2"> <p>可放大影像時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重設 </span> </p> </td> 
   <td colname="col2"> <p>當影像處於最大縮放層級，且可重設為初始狀態時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 拖曳 </span> </p> </td> 
   <td colname="col2"> <p>當使用者平移處於縮放狀態的影像時顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

