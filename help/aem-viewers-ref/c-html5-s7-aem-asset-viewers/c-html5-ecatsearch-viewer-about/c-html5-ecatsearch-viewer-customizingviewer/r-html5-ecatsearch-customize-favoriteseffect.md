---
title: 收藏夾效果
description: 查看器在主視圖上顯示「收藏夾」表徵圖，位於用戶最初添加該表徵圖的位置。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 7603c873-a2d1-4a24-85a6-8e56a1f207de
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# 收藏夾效果{#favorites-effect}

查看器在主視圖上顯示「收藏夾」表徵圖，位於用戶最初添加該表徵圖的位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

「收藏夾」表徵圖的外觀由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon
```

**收藏夾表徵圖的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p> 為表徵圖顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS浮雕，則在圖稿浮雕內定位。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS繁體 </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>表徵圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>表徵圖的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定36 x 36像素收藏夾表徵圖。

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

在台式機系統上，該元件支援 `cursortype` 屬性選擇器，可以應用到 `.s7favoriteseffect` 類，並根據所選用戶操作控制游標的類型。 以下 `cursortype` 值受支援：

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 模式_添加 </span> </p> </td> 
   <td colname="col2"> <p>顯示的用戶正在添加新的「收藏夾」表徵圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 模式刪除 </span> </p> </td> 
   <td colname="col2"> <p>顯示的用戶正在刪除現有收藏夾表徵圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 模式視圖 </span> </p> </td> 
   <td colname="col2"> <p>當收藏夾編輯未處於活動狀態時，以正常操作模式顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 每種類型的元件狀態具有不同的滑鼠游標。

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
