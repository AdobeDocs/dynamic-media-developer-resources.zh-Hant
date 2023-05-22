---
title: 字幕
description: 視頻查看器的URL命令。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: a9af3335-ae18-4399-9014-47ec0306a087
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 8%

---

# 字幕{#caption}

視頻查看器的URL命令。

` caption= *`file`*[,0|1]`

查看器支援通過托管WebVTT檔案進行隱藏字幕。 不支援重疊的提示和區域。 支援的提示定位運算子包括以下內容：

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
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>文本對齊 </p> </td> 
   <td colname="col3"> <p><span class="codeph"> 左|右|中|開始|結束</span> </p> </td> 
   <td colname="col4"> <p> 控制文本對齊。 </p> <p>預設值為 <span class="codeph"> 中</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>文本位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 在VideoPlayer元件中設定標題文本開頭的百分比。 </p> <p>預設值為0%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>行大小 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 用於字幕的視頻寬度的百分比。 </p> <p>預設為100%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整數 </p> </td> 
   <td colname="col4"> <p> 確定頁面上的行位置。 </p> <p>如果它表示為整數（無百分號），則表示顯示文本的頂部的行數。 </p> <p>如果是百分比（百分號是最後一個字元），則標題文本將顯示在顯示區域的下方。 </p> <p>預設為100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>

不支援WebVTT檔案中存在的其他WebVTT功能，但不應中斷字幕。

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> file</span></span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT標題內容的URL或路徑。 通過ImageServing提供WebVTT檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 指定預設標題狀態(啟用為 <span class="codeph"> 1</span>)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

無。

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
