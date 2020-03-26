---
description: 主視圖由目錄影像組成。 您可以滑動它以移至其他頁面或縮放。
seo-description: 主視圖由目錄影像組成。 您可以滑動它以移至其他頁面或縮放。
seo-title: 頁面檢視
solution: Experience Manager
title: 頁面檢視
topic: Dynamic media
uuid: f585bf57-c66a-4213-a2af-d9625beb5bed
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 頁面檢視{#page-view}

主視圖由目錄影像組成。 您可以滑動它以移至其他頁面或縮放。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

檢視區域的外觀會使用下列CSS類別選擇器加以控制：

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 以十六進位格式顯示主視圖的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 游標 </span> </p> </td> 
   <td colname="col2"> <p>顯示在主視圖上的游標。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——使主視圖透明。

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

在案頭系統上，元件支 `cursortype` 持屬性選擇器，該選擇器可應用 `.s7pageview` 於類，並基於元件狀態和用戶操作控制游標的類型。 The following `cursortype` values are supported:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p>當影像因影像解析度小、元件設定或兩者皆無法縮放時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 牛 </span> </p> </td> 
   <td colname="col2"> <p>可放大影像時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重設 </span> </p> </td> 
   <td colname="col2"> <p>當影像處於最大縮放層級時顯示，並可重設為初始狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 拖曳 </span> </p> </td> 
   <td colname="col2"> <p>當使用者平移處於縮放狀態的影像時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 投影片 </span> </p> </td> 
   <td colname="col2"> <p>當使用者透過水準滑動或輕拂來執行影像切換時顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以視覺化方式分隔目錄跨頁的左和右頁面的分頁線，由下列CSS類別選擇器控制：

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 頁面分隔線的寬度。 設為 <span class="codeph"> 0 px </span> 可完全隱藏分隔線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p>您要用作分頁符的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——使用半透明影像來製作40像素寬的分頁線。

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>當修飾 `frametransition` 元設為或 `turn` (在案頭 `auto` 系統上)時，頁面分隔線的外觀會由修飾元控制， `pageturnstyle` 而 `.s7pagedivider` CSS類別則會被忽略。

您可以在主檢視器區域上設定自訂滑鼠游標的顯示。 這是由套用至 `.s7ecatalogsearchviewer .s7pageview` CSS類別的其他屬性選擇器所控制：

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p> 通常是箭頭，針對不可縮放的影像顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 牛 </span> </p> </td> 
   <td colname="col2"> <p> 顯示影像何時可放大。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重設 </span> </p> </td> 
   <td colname="col2"> <p>顯示影像在最大縮放時可重設的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 拖曳 </span> </p> </td> 
   <td colname="col2"> <p>顯示使用者在影像中縮放時執行拖曳作業的時間 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 投影片 </span> </p> </td> 
   <td colname="col2"> <p>顯示使用者何時使用投影片手勢執行影像交換 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——每種類型的元件狀態有不同的滑鼠游標。

```
.s7ecatalogsearchviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```

