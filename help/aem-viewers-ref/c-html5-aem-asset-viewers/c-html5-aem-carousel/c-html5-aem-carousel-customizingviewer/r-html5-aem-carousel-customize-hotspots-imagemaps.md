---
description: 檢視器會在主檢視上顯示熱點圖示，這些熱點原本是在AEM AssetsDynamic Media-隨選地區製作的。
solution: Experience Manager
title: 熱點和影像映射
feature: Dynamic Media經典，檢視器，SDK/API，轉盤橫幅
role: 開發人員，商業從業人員
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 1%

---

# 熱點和影像映射{#hotspots-and-image-maps}

檢視器會在主檢視上顯示熱點圖示，這些熱點原本是在AEM AssetsDynamic Media-隨選地區製作的。

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
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p>熱點表徵圖圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p>如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 背景  </span> </p> </td> 
   <td colname="col2"> <p>影像地圖區域填滿顏色。 </p> <p>以<span class="codeph"> #RRGGBB </span>、<span class="codeph"> RGB(R,G,B)</span>或<span class="codeph"> RGBA(R,G,B,A)</span>格式指定此顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>影像地圖區域填滿顏色。 </p> <p>以<span class="codeph"> #RRGGBB </span>、<span class="codeph"> RGB(R,G,B)</span>或<span class="codeph"> RGBA(R,G,B,A)</span>格式指定此顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> 影像地圖區域邊框樣式。 應指定為" <span class="codeph"> width </span> <span class="codeph"> solid color </span>"，其中<span class="codeph"> width </span>以像素表示，<span class="codeph"> color </span>設為<span class="codeph"> #RRGBB </span>, <span class="codeph"> RGB(R,G,B))</span>或<span class="codeph"> RGBA(R,G,B,A)</span>。 </p> </td> 
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
