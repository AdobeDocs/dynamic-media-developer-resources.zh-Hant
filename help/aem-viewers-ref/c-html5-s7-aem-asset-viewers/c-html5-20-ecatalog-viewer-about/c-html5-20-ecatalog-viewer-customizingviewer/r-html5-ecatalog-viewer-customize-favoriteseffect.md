---
description: 檢視器會在主檢視上顯示「我的最愛」圖示，位於使用者最初新增的位置。
solution: Experience Manager
title: 收藏夾效果
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,User
exl-id: e87226cf-56bf-4d54-8df5-91295eae90a8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# 收藏夾效果{#favorites-effect}

檢視器會在主檢視上顯示「我的最愛」圖示，位於使用者最初新增的位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

「收藏夾」表徵圖的外觀由以下CSS類選擇器控制：

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**「收藏夾」表徵圖的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p> 為表徵圖顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>圖示的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>圖示的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：設定36 x 36像素我的最愛圖示。

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

在案頭系統上，該元件支援`cursortype`屬性選擇器，可將其應用於`.s7favoriteseffect`類，並根據所選用戶操作控制游標的類型。 支援下列`cursortype`值：

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add  </span> </p> </td> 
   <td colname="col2"> <p>顯示的用戶正在添加新的收藏夾表徵圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove  </span> </p> </td> 
   <td colname="col2"> <p>顯示的用戶正在刪除現有的收藏夾表徵圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view  </span> </p> </td> 
   <td colname="col2"> <p>當「收藏夾」編輯不活動時，以正常操作模式顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 每種類型的元件狀態有不同的滑鼠游標。

```
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```
