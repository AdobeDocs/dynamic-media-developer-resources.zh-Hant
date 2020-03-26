---
description: 檢視器會在主檢視上顯示熱點圖示，這些熱點原本是在AEM Assets的Dynamic Media —— 隨選中製作的地方。
seo-description: 檢視器會在主檢視上顯示熱點圖示，這些熱點原本是在AEM Assets的Dynamic Media —— 隨選中製作的地方。
seo-title: 熱點和影像映射
solution: Experience Manager
title: 熱點和影像映射
topic: Dynamic media
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 熱點和影像映射{#hotspots-and-image-maps}

檢視器會在主檢視上顯示熱點圖示，這些熱點原本是在AEM Assets的Dynamic Media —— 隨選中製作的地方。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

熱點表徵圖的外觀由下列CSS類別選擇器控制：

```
.s7carouselviewer .s7imagemapeffect .s7icon
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p>熱點表徵圖圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p>如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>熱點表徵圖寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>熱點表徵圖高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——設定56 x 56像素熱點表徵圖，該表徵圖顯示兩個不同表徵圖狀態中每個狀態的不同影像：

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**影像地圖區域的CSS屬性**

使用下列CSS類別選取器來控制影像地圖區域的外觀：

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 </span> </p> </td> 
   <td colname="col2"> <p>影像地圖區域填滿顏色。 </p> <p>以 <span class="codeph"> #RRGGBB </span>、 <span class="codeph"> RGB(R,G,B) </span>或 <span class="codeph"> RGBA(R,G,B,A)格式指定此顏色 </span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>影像地圖區域填滿顏色。 </p> <p>以 <span class="codeph"> #RRGGBB </span>、 <span class="codeph"> RGB(R,G,B) </span>或 <span class="codeph"> RGBA(R,G,B,A)格式指定此顏色 </span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> 影像地圖區域邊框樣式。 應指定為寬度 <span class="codeph"> 實色 </span> "，其中寬度以像素表示，其中 <span class="codeph"> "寬度以像素表示， </span>" <span class="codeph"> #RRBB,B,B,B,B,B, </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>G，或RGBA(R,G,D,D);B,B,A,D,D,B,D.D.D.D.D.D.D.D.D.D.B.B.D.D.B.D.B.B.D.B.B.D.D.D.D.D.D.D.D.D.D.D.D.D.D.R.R.B.D.D.D.B.D.D.D.D.D.B.D.D. </p> </td> 
  </tr> 
 </tbody> 
</table>

範例——使用一個像素黑邊框來設定透明影像地圖區域：

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

