---
description: 主視圖包含目錄映像。 可以滑動它來前往其他頁面或放大。
solution: Experience Manager
title: 頁面檢視
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 4%

---

# 頁面檢視{#page-view}

主視圖包含目錄映像。 可以滑動它來前往其他頁面或放大。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

查看區域的外觀由以下CSS類選擇器控制：

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
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 以十六進位格式顯示主視圖的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 游標  </span> </p> </td> 
   <td colname="col2"> <p>顯示在主視圖上的游標。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使主視圖透明。

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

在案頭系統上，元件支援`cursortype`屬性選擇器，該選擇器可應用於`.s7pageview`類，並根據元件狀態和用戶操作控制游標的類型。 支援下列`cursortype`值：

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
   <td colname="col1"> <p> <span class="codeph"> 左敏  </span> </p> </td> 
   <td colname="col2"> <p>可放大影像時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重設 </span> </p> </td> 
   <td colname="col2"> <p>當影像處於最大縮放級別時顯示，可重置為初始狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 拖曳 </span> </p> </td> 
   <td colname="col2"> <p>當使用者平移處於縮放狀態的影像時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻燈片  </span> </p> </td> 
   <td colname="col2"> <p>當用戶通過水準滑動或輕觸執行影像交換時顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以視覺化方式分隔目錄跨頁的左和右頁面的分隔線，由下列CSS類別選取器控制：

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
   <td colname="col2"> <p> 頁面分隔線的寬度。 設為<span class="codeph"> 0 </span> px ，以完全隱藏分隔線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>您要用作分頁器的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：若要有40像素寬的頁面分隔線，且具有半透明影像。

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>當`frametransition`修飾符設定為`turn`或`auto`（在案頭系統上）時，使用`pageturnstyle`修飾符控制頁面分隔符的外觀，並忽略`.s7pagedivider` CSS類。

可以在主查看器區域上配置自定義滑鼠游標的顯示。 可透過套用至`.s7ecatalogsearchviewer .s7pageview` CSS類別的其他屬性選取器來控制：

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 預設  </span> </p> </td> 
   <td colname="col2"> <p> 通常為非可縮放影像的箭頭。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左敏  </span> </p> </td> 
   <td colname="col2"> <p> 顯示影像何時可放大。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重設 </span> </p> </td> 
   <td colname="col2"> <p>顯示影像何時達到最大縮放並可重設。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 拖曳 </span> </p> </td> 
   <td colname="col2"> <p>顯示用戶何時對影像中的縮放執行拖動操作 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻燈片  </span> </p> </td> 
   <td colname="col2"> <p>顯示使用者何時使用投影片手勢執行影像交換 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 每種類型的元件狀態有不同的滑鼠游標。

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
