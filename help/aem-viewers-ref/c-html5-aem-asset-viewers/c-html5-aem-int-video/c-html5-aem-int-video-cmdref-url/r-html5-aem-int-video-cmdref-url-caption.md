---
description: 互動式視訊檢視器的URL命令。
solution: Experience Manager
title: 字幕
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: 8eb2aa50-52b9-4b63-9789-87e492f34a22
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 7%

---

# 字幕{#caption}

互動式視訊檢視器的URL命令。

` caption= *`file`*[,0|1]`

檢視器透過托管WebVTT檔案支援隱藏式字幕。 不支援重疊的提示和區域。 支援的提示定位操作器包括：

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
   <td colname="col2"> <p>文字對齊 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end  </span> </p> </td> 
   <td colname="col4"> <p> 控制文本對齊方式。 </p> <p>預設值為<span class="codeph">中間</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>文字位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> VideoPlayer元件中字幕文字開頭的插入百分比。 </p> <p>預設為0%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S  </span> </p> </td> 
   <td colname="col2"> <p>行大小 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 用於字幕的視頻寬度百分比。 </p> <p>預設為100%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整數 </p> </td> 
   <td colname="col4"> <p> 決定頁面上的行位置。 </p> <p>如果以整數（無百分比符號）表示，則為顯示文字的上方的行數。 </p> <p>如果是百分比（百分比符號是最後一個字元），則字幕文本將在顯示區域下顯示該百分比。 </p> <p>預設為100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTT檔案中存在的其他WebVTT功能不受支援，但不應中斷字幕。

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 檔案  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT標題內容的URL或路徑。 依影像伺服提供WebVTT檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定預設字幕狀態（啟用為<span class="codeph"> 1 </span>）。 </p> </td> 
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
