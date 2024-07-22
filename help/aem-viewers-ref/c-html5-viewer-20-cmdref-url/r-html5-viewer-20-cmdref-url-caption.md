---
title: 註解
description: 所有檢視器通用的引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# 註解{#caption}

所有檢視器通用的引數。

>[!NOTE]
>
>這個命令不適用於Video Image Viewer。

` caption= *`檔案`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">檔案</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT插圖示題內容的URL或路徑。 「影像伺服」會提供WebVTT檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 指定預設註解狀態。 啟用的是<span class="codeph"> 1 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

此檢視器透過託管的WebVTT檔案支援隱藏式字幕。 透過此引數指定的註解會套用至媒體集中排名第一的視訊；後續的視訊播放時不會加上註解。 不支援重疊的提示和區域。 支援的提示定位運運算元：

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
   <td colname="col2"> <p>測試對齊 </p> </td> 
   <td colname="col3"> <p> <span class="codeph">靠左|靠右|中間|開始|結束</span> </p> </td> 
   <td colname="col4"> <p> 控制文字的對齊方式。 </p> <p>預設為<span class="codeph">中間的</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>文字位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 註解文字開頭插入VideoPlayer元件的百分比。 </p> <p>預設值為<span class="codeph"> 0% </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>行大小 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 用於註解的視訊寬度百分比。 </p> <p>預設值為<span class="codeph"> 100% </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> 決定頁面上的行位置。 </p> <p>如果以不含百分比符號的整數來表示，則為文字顯示位置上方的行數。 </p> <p>如果以百分比表示 — 百分比符號是最後一個字元 — 則註解文字會以百分比顯示在顯示區域中。 </p> <p>預設值為<span class="codeph"> 100% </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

如果WebVTT檔案中存在任何其他WebVTT功能，則不支援這些功能；但是，它們不會中斷字幕功能。

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">檔案</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定URL或WebVTT插圖示題內容的路徑。 WebVTT檔案是由「影像伺服」提供。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 指定預設註解狀態。 </p> <p>啟用的是<span class="codeph"> 1 </span>。 </p> </td> 
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
