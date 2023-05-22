---
title: 收藏夾菜單
description: 「收藏夾」(Favorites)菜單下拉清單出現在控制欄中。 它由一個按鈕和一個面板組成，當用戶按一下或輕擊某個按鈕時，面板會展開。 該面板包含單個收藏夾工具。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 129a8451-f634-44ad-adb1-f30d2621cb29
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# 收藏夾菜單{#favorites-menu}

「收藏夾」(Favorites)菜單下拉清單出現在控制欄中。 它由一個按鈕和一個面板組成，當用戶按一下或輕擊某個按鈕時，面板會展開。 該面板包含單個收藏夾工具。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

查看器用戶介面中「收藏夾」菜單的位置和大小由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7favoritesmenu
```

**「收藏夾」菜單按鈕的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上邊距 </span> </p> </td> 
   <td colname="col2"> <p> 從控制欄頂部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊距 </span> </p> </td> 
   <td colname="col2"> <p> 到左邊的下一個按鈕的距離，如果此按鈕是行中的第一個按鈕，則到控制欄的左側的距離。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定「收藏夾」菜單，該菜單從控制欄頂部放置四個像素，從最靠近的按鈕放置十個像素，大小為28 x 28像素。

```
.s7ecatalogsearchviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

「收藏夾」菜單按鈕的外觀由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton
```

**「收藏夾」按鈕的CSS屬性**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p> 為給定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS浮雕，則在圖稿浮雕內定位。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS繁體 </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可用於將不同外觀應用於不同按鈕狀態。

按鈕工具提示可以本地化。 請參閱 [用戶介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 的子菜單。

示例 — 設定「收藏夾」菜單按鈕，該按鈕顯示四個不同按鈕狀態中每個狀態的不同影像。

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

包含單個「收藏夾」表徵圖的面板的外觀由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel
```

**「收藏夾」菜單面板的CSS屬性**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>面板的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定具有透明顏色的面板。

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```
