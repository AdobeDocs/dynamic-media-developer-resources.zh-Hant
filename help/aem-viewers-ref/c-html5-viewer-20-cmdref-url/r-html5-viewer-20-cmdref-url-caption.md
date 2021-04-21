---
description: 所有檢視器通用的參數。
solution: Experience Manager
title: 標題
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 6%

---

# 標題{#caption}

所有檢視器通用的參數。

>[!NOTE]
>
>此命令不適用於視頻影像查看器。

` caption= *`file`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 檔案  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT標題內容的URL或路徑。 影像伺服功能可支援WebVTT檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定預設標題狀態。 已啟用<span class="codeph"> 1 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

此檢視器支援透過代管WebVTT檔案的隱藏字幕。 使用此參數指定的標題適用於媒體集中最先出現的視訊；後續視訊播放時不含標題。 不支援重疊的提示和區域。 支援的提示定位運算子：

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
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end  </span> </p> </td> 
   <td colname="col4"> <p> 控制文字的對齊方式。 </p> <p>預設值為<span class="codeph">中間</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>文字位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 在VideoPlayer元件中插入標題文字開頭的百分比。 </p> <p>預設值為<span class="codeph"> 0% </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S  </span> </p> </td> 
   <td colname="col2"> <p>行大小 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 用於標題的視訊寬度百分比。 </p> <p>預設值為<span class="codeph"> 100% </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整數 </p> </td> 
   <td colname="col4"> <p> 確定頁面上的行位置。 </p> <p>如果它表示為無百分比符號的整數，則表示顯示文本的頂部的行數。 </p> <p>如果以百分比表示，百分比符號是最後一個字元，則標題文字會顯示在顯示區域的百分比下。 </p> <p>預設值為<span class="codeph"> 100% </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

請注意，如果WebVTT檔案中有其他WebVTT功能，則不支援這些功能；但是不會中斷字幕。

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 檔案  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT標題內容的URL或路徑。 WebVTT檔案由影像伺服提供。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定預設標題狀態。 </p> <p>已啟用<span class="codeph"> 1 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選填。

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

無。

## 範例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
