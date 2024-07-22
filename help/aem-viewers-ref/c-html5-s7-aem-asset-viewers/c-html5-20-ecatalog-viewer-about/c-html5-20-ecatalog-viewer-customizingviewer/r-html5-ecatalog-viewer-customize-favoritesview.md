---
title: 我的最愛檢視
description: 我的最愛檢視由一欄縮圖影像組成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 10536242-1015-49ff-ae27-59671f30d886
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# 我的最愛檢視{#favorites-view}

我的最愛檢視由一欄縮圖影像組成。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

「我的最愛」檢視容器的外觀是由下列CSS類別選取器所控制：

```
.s7ecatalogviewer .s7favoritesview
```

收藏夾檢視的位置和高度由檢視管理；在CSS中只能定義寬度。

我的最愛檢視的&#x200B;**CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p> 我的最愛檢視的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>檢視寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定寬度為100畫素且背景為半透明灰色的「我的最愛」檢視：

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

我的最愛縮圖之間的間距由下列CSS類別選取器控制：

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

我的最愛縮圖的&#x200B;**CSS屬性**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">利潤</span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖周圍垂直邊界的大小。 實際縮圖間距等於為<span class="codeph"> .s7縮圖儲存格</span>設定的上下邊界總和。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定十個畫素間距：

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

使用下列CSS類別選取器來控制個別縮圖的外觀：

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

我的最愛縮圖的&#x200B;**CSS屬性**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>縮圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>縮圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">邊框</span> </p> </td> 
   <td colname="col2"> <p>縮圖的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援`state`屬性選取器，可用來將不同的外觀元素套用至不同的縮圖狀態。 特別是，`state="selected"`對應於使用者最近選取的縮圖。 屬性`state="default"`對應到其餘的縮圖。 而且，屬性`state="over"`用於滑鼠懸停上。

範例 — 若要設定75 x 75畫素的縮圖、淺灰色的預設框線以及深灰色的選取框線：

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

縮圖示籤的外觀是由下列CSS類別選取器所控制：

```
.s7ecatalogviewer .s7favoritesview .s7label
```

我的最愛標籤&#x200B;**的** CSS屬性

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字型大小</span> </p> </td> 
   <td colname="col2"> <p>字型大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定14畫素Helvetica®字型的標籤：

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
