---
description: 互動式視訊檢視器的URL命令。
solution: Experience Manager
title: 標題
feature: Dynamic Media經典，檢視器，SDK/API，互動式視訊
role: 開發人員，商業從業人員
exl-id: 8eb2aa50-52b9-4b63-9789-87e492f34a22
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 7%

---

# 標題{#caption}

互動式視訊檢視器的URL命令。

` caption= *`file`*[,0|1]`

檢視器支援透過代管WebVTT檔案的隱藏字幕。 不支援重疊的提示和區域。 支援的提示定位運算子包括：

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>索引鍵 </p> </th> 
   <th colname="col2" class="entry"> <p>名稱 </p> </th> 
   <th colname="col3" class="entry"> <p>值 </p> </th> 
   <th colname="col4" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>文本對齊 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end  </span> </p> </td> 
   <td colname="col4"> <p> 控制文字對齊。 </p> <p>預設值為<span class="codeph">中間</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>文字位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 在VideoPlayer元件中插入標題文字開頭的百分比。 </p> <p>預設值為0%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S  </span> </p> </td> 
   <td colname="col2"> <p>行大小 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 用於標題的視訊寬度百分比。 </p> <p>預設值為100%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整數 </p> </td> 
   <td colname="col4"> <p> 確定頁面上的行位置。 </p> <p>如果它表示為整數（無百分比符號），則表示顯示文本的頂部的行數。 </p> <p>如果是百分比（百分比符號是最後一個字元），則標題文字會顯示在顯示區域的百分比下。 </p> <p>預設值為100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTT檔案中的其他WebVTT功能不受支援，但不應中斷字幕功能。

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 檔案  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT標題內容的URL或路徑。 依影像伺服提供WebVTT檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定預設標題狀態（啟用為<span class="codeph"> 1 </span>）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選填。

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

無。

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.caption.vtt,1
```
