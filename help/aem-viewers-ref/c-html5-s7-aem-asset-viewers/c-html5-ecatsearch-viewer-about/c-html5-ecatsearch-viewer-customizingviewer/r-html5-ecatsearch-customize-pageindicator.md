---
description: 頁面指示器顯示當前頁面索引和總頁數。 它顯示在案頭系統和平板電腦的主控制欄中，在行動電話上，它被添加到輔助控制欄中。 頁面指標可由CSS調整大小、加上外觀和定位。
solution: Experience Manager
title: 頁面指標
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 4%

---

# 頁面指標{#page-indicator}

頁面指示器顯示當前頁面索引和總頁數。 它顯示在案頭系統和平板電腦的主控制欄中，在行動電話上，它被添加到輔助控制欄中。 頁面指標可由CSS調整大小、加上外觀和定位。

外觀頁面指示器由以下CSS類選擇器控制：

`.s7ecatalogsearchviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>從主控制欄（在案頭系統和平板電腦上）或次控制欄（在行動電話上）的上邊框位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p>從主控制欄（在案頭系統和平板電腦上）或次控制欄（在行動電話上）的右邊框定位，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p>從主控制欄（在案頭系統和平板電腦上）或次控制欄（在行動電話上）的左邊框位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從主控制欄（在案頭系統和平板電腦上）或次控制欄（在行動電話上）的底邊框位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>頁面指示器的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>頁面指示器的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>字型色彩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要設定一個56 x 28像素、水準居中並從主控制欄底部定位4像素的頁面指示器，並使用14像素Helvetica字型。

```
.s7ecatalogsearchviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```
