---
title: 收藏夾菜單
description: 「收藏夾」菜單下拉清單出現在控制欄中。 它包含按鈕和面板，當使用者點按或點按按鈕時會展開。 此面板包含個別的我的最愛工具。
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

「收藏夾」菜單下拉清單出現在控制欄中。 它包含按鈕和面板，當使用者點按或點按按鈕時會展開。 此面板包含個別的我的最愛工具。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

檢視器使用者介面中「我的最愛」功能表的位置和大小由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7favoritesmenu
```

**「收藏夾」菜單按鈕的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距上 </span> </p> </td> 
   <td colname="col2"> <p> 從控制欄頂端的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊距 </span> </p> </td> 
   <td colname="col2"> <p> 左側的下一個按鈕的距離，或者控制欄左側的距離（如果此按鈕是行中的第一個按鈕）。 </p> </td> 
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

範例 — 設定「我的最愛」功能表，該功能表位於控制列頂端的四個像素，以及最靠左的按鈕上的十個像素，大小為28 x 28像素。

```
.s7ecatalogsearchviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

使用以下CSS類選擇器控制「收藏夾」菜單按鈕的外觀：

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton
```

**「收藏夾」按鈕的CSS屬性**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像 </span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選取器，可用來將不同的外觀套用至不同的按鈕狀態。

按鈕工具提示可以本地化。 請參閱 [用戶介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 以取得更多資訊。

範例 — 設定一個「我的最愛」功能表按鈕，該按鈕會針對四個不同的按鈕狀態中的每一個顯示不同的影像。

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

包含個別「我的最愛」圖示的面板外觀由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel
```

**「收藏夾」菜單面板的CSS屬性**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色 </span> </p> </td> 
   <td colname="col2"> <p>面板的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：設定面板以使用透明顏色。

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```
