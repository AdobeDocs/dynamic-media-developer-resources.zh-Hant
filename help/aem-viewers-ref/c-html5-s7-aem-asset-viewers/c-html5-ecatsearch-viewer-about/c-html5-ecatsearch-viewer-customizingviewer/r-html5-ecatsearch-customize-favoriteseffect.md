---
description: 檢視器會在主檢視上顯示「我的最愛」圖示，位於使用者原本新增的位置。
solution: Experience Manager
title: 我的最愛效果
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---


# 我的最愛效果{#favorites-effect}

檢視器會在主檢視上顯示「我的最愛」圖示，位於使用者原本新增的位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

「我的最愛」圖示的外觀會由下列CSS類別選擇器控制：

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon
```

**「我的最愛」圖示的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p> 為表徵圖顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>圖示寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>圖示的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——設定36 x 36像素「我的最愛」圖示。

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

在案頭系統上，該元件支援`cursortype`屬性選擇器，您可以將該選擇器應用於`.s7favoriteseffect`類，並根據選定的用戶操作控制游標類型。 支援下列`cursortype`值：

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
   <td colname="col2"> <p>當「我的最愛」編輯未作用時，會以正常操作模式顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——每種類型的元件狀態有不同的滑鼠游標。

```
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```

