---
description: 「我的最愛」檢視包含一欄縮圖影像。
solution: Experience Manager
title: 我的最愛檢視
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 2%

---


# 我的最愛檢視{#favorites-view}

「我的最愛」檢視包含一欄縮圖影像。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

我的最愛檢視容器的外觀是由下列CSS類別選擇器所控制：

```
.s7ecatalogsearchviewer .s7favoritesview
```

「收藏夾」視圖的位置和高度由視圖管理；在CSS中，只能定義寬度。

**「我的最愛」檢視的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p> 「我的最愛」檢視的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>視圖寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——設定寬度為100像素且半透明灰色背景的「我的最愛」檢視。

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

「我的最愛」縮圖之間的間距會由下列CSS類別選擇器控制：

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**我的最愛縮圖的CSS屬性**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖的垂直邊界大小。 實際縮圖間距等於為<span class="codeph"> .s7thumbcell </span>設定的上下邊界之和。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——設定10像素間距。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

個別縮圖的外觀由下列CSS類別選擇器控制：

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**我的最愛縮圖的CSS屬性**

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
   <td colname="col2"> <p>縮圖邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援`state`屬性選擇器，可用來將不同的外觀套用至不同的縮圖狀態。 特別是，`state="selected"`對應於使用者最近選取的縮圖。 `state="default"` 對應其餘的縮圖。而`state="over"`則用於滑鼠暫留。

範例——若要設定75 x 75像素的縮圖，請使用淺灰色預設邊框和深灰色選取的邊框。

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

縮表徵圖簽的外觀由下列CSS類別選擇器控制：

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**「我的最愛」標籤的CSS屬性**

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

示例——使用14像素Helvetica字型設定標籤。

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

