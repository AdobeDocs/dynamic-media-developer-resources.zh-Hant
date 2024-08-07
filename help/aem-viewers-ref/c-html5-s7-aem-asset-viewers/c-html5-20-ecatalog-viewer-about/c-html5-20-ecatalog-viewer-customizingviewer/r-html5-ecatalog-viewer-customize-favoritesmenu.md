---
title: 我的最愛功能表
description: 「我的最愛」功能表下拉式清單會出現在控制列中。 它由按鈕和面板組成，當使用者按一下或點選按鈕時，面板會展開。 面板包含個別「我的最愛」工具。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3c90320-b6fc-4a43-b75f-d39234b1e73c
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# 我的最愛功能表{#favorites-menu}

「我的最愛」功能表下拉式清單會出現在控制列中。 它由按鈕和面板組成，當使用者按一下或點選按鈕時，面板會展開。 面板包含個別「我的最愛」工具。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

檢視器使用者介面中「我的最愛」功能表的位置和大小由下列CSS類別選取器控制：

```
.s7ecatalogviewer .s7favoritesmenu
```

[我的最愛]功能表按鈕的&#x200B;**CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上邊界</span> </p> </td> 
   <td colname="col2"> <p> 從控制列頂端的位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">左邊界</span> </p> </td> 
   <td colname="col2"> <p> 與左側或控制列左側的下一個按鈕的距離（如果這是列中的第一個按鈕）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>按鈕的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定「我的最愛」功能表，使其位於控制列上方的四個畫素，最接近的按鈕左側十個畫素，大小為28 x 28畫素：

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

「我的最愛」功能表按鈕的外觀是由下列CSS類別選取器所控制：

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

[我的最愛]按鈕的&#x200B;**CSS屬性**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景影像</span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS拼寫，則定位在圖稿sprite內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選取器，可用來將不同的外觀元素套用至不同的按鈕狀態。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

範例 — 設定「我的最愛」功能表按鈕，針對四種不同按鈕狀態分別顯示不同的影像：

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

包含個別「我的最愛」圖示的面板外觀可由下列CSS類別選取器控制：

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

[我的最愛]功能表面板的&#x200B;**CSS屬性**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p>面板的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定面板為透明顏色：

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```
