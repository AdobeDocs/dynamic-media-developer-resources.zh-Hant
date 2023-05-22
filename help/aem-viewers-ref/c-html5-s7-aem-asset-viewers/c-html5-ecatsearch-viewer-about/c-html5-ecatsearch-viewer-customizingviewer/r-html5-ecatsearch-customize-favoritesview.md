---
title: 收藏夾視圖
description: 收藏夾視圖由縮略影像的列組成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 8daf3d19-615b-4d62-a6f5-6a153d193b88
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---

# 收藏夾視圖{#favorites-view}

收藏夾視圖由縮略影像的列組成。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

收藏夾視圖容器的外觀由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7favoritesview
```

「收藏夾」視圖的位置和高度由視圖管理；在CSS中，只能定義寬度。

**收藏夾視圖的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 「收藏夾」視圖的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>視圖寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定寬度為100像素、半透明灰色背景的「收藏夾」視圖。

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

「收藏夾」縮略圖之間的間距由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**收藏夾縮略圖的CSS屬性**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每個縮覽圖周圍的垂直邊距的大小。 實際縮略圖間距等於為設定的上邊距和下邊距之和 <span class="codeph"> .s7拇指單元 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定十個像素間距。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

單個縮略圖的外觀由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**收藏夾縮略圖的CSS屬性**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮略圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮略圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>縮略圖的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮略圖支援 `state` 屬性選擇器，可用於將不同外觀應用於不同的縮略圖狀態。 特別是， `state="selected"` 對應於用戶最近選擇的縮略圖。 同時 `state="default"` 與其餘縮略圖相對應。 和 `state="over"` 用於滑鼠懸停。

示例 — 要設定75 x 75像素的縮略圖，請設定淺灰色預設邊框和深灰色選定邊框。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

縮略表徵圖簽的外觀由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**收藏夾標籤的CSS屬性**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型 </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小 </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定14像素Helvetica®字型的標籤。

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
