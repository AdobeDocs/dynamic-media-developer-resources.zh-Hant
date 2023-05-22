---
title: 字幕
description: 所有查看器通用的參數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 6%

---

# 字幕{#caption}

所有查看器通用的參數。

>[!NOTE]
>
>此命令不適用於視頻影像查看器。

` caption= *`file`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 檔案 </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT標題內容的URL或路徑。 Image Serving服務用於WebVTT檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定預設標題狀態。 已啟用 <span class="codeph"> 1 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

此查看器支援通過托管WebVTT檔案進行隱藏字幕。 使用此參數指定的字幕適用於媒體集中最先出現的視頻；隨後播放的視頻沒有字幕。 不支援重疊的提示和區域。 支援的提示定位運算子：

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
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
   <td colname="col2"> <p>test對齊 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 左|右|中|開始|結束 </span> </p> </td> 
   <td colname="col4"> <p> 控制文本的對齊方式。 </p> <p>預設值為 <span class="codeph"> 中 </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>文本位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 在VideoPlayer元件中設定標題文本開頭的百分比。 </p> <p>預設值為 <span class="codeph"> 0% </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>行大小 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 用於字幕的視頻寬度的百分比。 </p> <p>預設值為 <span class="codeph"> 100% </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整數 </p> </td> 
   <td colname="col4"> <p> 確定頁面上的行位置。 </p> <p>如果它表示為無百分號的整數，則它是顯示文本的頂部的行數。 </p> <p>如果它以百分比表示 — 百分號是最後一個字元 — 則標題文本將顯示在顯示區域的下面百分比。 </p> <p>預設值為 <span class="codeph"> 100% </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

如果WebVTT檔案中存在其他WebVTT功能，則不支援這些功能；但是，它們不會干擾字幕。

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 檔案 </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT標題內容的URL或路徑。 WebVTT檔案由影像服務提供。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定預設標題狀態。 </p> <p>已啟用 <span class="codeph"> 1 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選擇性.

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

無。

## 範例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
