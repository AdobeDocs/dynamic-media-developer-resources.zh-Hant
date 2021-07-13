---
description: 收藏夾視圖包含一列縮略圖。
solution: Experience Manager
title: 收藏夾視圖
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,User
exl-id: 10536242-1015-49ff-ae27-59671f30d886
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 2%

---

# 收藏夾視圖{#favorites-view}

收藏夾視圖包含一列縮略圖。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

「收藏夾」視圖容器的外觀由以下CSS類選擇器控制：

```
.s7ecatalogviewer .s7favoritesview
```

「收藏夾」視圖的位置和高度由視圖管理；在CSS中，只能定義寬度。

**收藏夾視圖的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 「收藏夾」視圖的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>檢視的寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定半透明灰色背景為100像素寬的收藏夾視圖。

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

「收藏夾」縮圖之間的間距由以下CSS類選擇器控制：

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**CSS屬性收藏夾縮略圖**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖周圍的垂直邊界大小。 實際縮圖間距等於為<span class="codeph"> .s7thumbcell </span>設定的上下邊界之和。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定10像素間距。

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

個別縮圖的外觀由下列CSS類別選取器控制：

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**CSS屬性收藏夾縮略圖**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 寬度  </span> </p> </td> 
   <td colname="col2"> <p>縮圖寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>縮圖的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援`state`屬性選取器，可用來將不同外觀套用至不同的縮圖狀態。 尤其`state="selected"`對應於使用者最近選取的縮圖。 `state="default"` 對應至縮圖的其餘部分。而`state="over"`用於滑鼠暫留。

範例 — 若要設定縮圖，縮圖為75 x 75像素、有淺灰色預設邊框和深灰色選取的邊框。

```
.s7ecatalogviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

縮表徵圖簽的外觀由下列CSS類選擇器控制：

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**收藏夾標籤的CSS屬性**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
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

示例 — 用14像素Helvetica字型設定標籤。

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
