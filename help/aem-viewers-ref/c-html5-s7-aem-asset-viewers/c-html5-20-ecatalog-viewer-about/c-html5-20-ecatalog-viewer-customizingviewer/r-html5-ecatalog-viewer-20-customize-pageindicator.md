---
description: 頁面指標會顯示目前的頁面索引和頁面總數。 它會顯示在桌上型電腦系統和平板電腦的主控制列，在行動電話上會新增至次要控制列。 頁面指示器可由CSS調整大小、改變外觀並定位。
seo-description: 頁面指標會顯示目前的頁面索引和頁面總數。 它會顯示在桌上型電腦系統和平板電腦的主控制列，在行動電話上會新增至次要控制列。 頁面指示器可由CSS調整大小、改變外觀並定位。
seo-title: 頁面指標
solution: Experience Manager
title: 頁面指標
topic: Dynamic media
uuid: 5e33c149-fdc7-419a-b5ff-b9be3f342d9f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 頁面指標{#page-indicator}

頁面指標會顯示目前的頁面索引和頁面總數。 它會顯示在桌上型電腦系統和平板電腦的主控制列，在行動電話上會新增至次要控制列。 頁面指示器可由CSS調整大小、改變外觀並定位。

頁面指示器的外觀由下列CSS類別選擇器控制：

`.s7ecatalogviewer .s7pageindicator`

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
   <td colname="col2"> <p>從主控制列（在桌上型電腦系統和平板電腦上）或次控制列（在行動電話上）的上邊框定位，包括間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p>從主控制列（在桌上型電腦系統和平板電腦上）或次控制列（在行動電話上）的右邊框定位，包括填補空白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p>從主控制列（在桌上型電腦系統和平板電腦上）或次控制列（在行動電話上）的左邊框放置，包括間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從主控制列（在桌上型電腦系統和平板電腦上）或次控制列（在行動電話上）的底邊框中定位，包括間距。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小 </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——若要設定56 x 28像素、水準置中且位於主控制列底部4像素的頁面指標，並使用14像素的Helvetica字型。

```
.s7ecatalogviewer  .s7pageindicator { 
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

