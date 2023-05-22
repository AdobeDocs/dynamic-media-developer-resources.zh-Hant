---
title: 熱點和影像映射
description: 查看器在主視圖上顯示熱點表徵圖，這些熱點最初是在AEM AssetsDynamic Media創作的，是按需的。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---

# 熱點和影像映射{#hotspots-and-image-maps}

查看器在主視圖上顯示熱點表徵圖，這些熱點最初是在AEM AssetsDynamic Media創作的，是按需的。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

熱點表徵圖的外觀由以下CSS類選擇器控制：

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
   <td colname="col2"> <p>如果使用CSS浮雕，則在圖稿浮雕內定位。 </p> <p>請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS繁體 </a>。 </p> </td> 
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

示例 — 設定56 x 56像素熱點表徵圖，該表徵圖顯示兩個不同表徵圖狀態中每個狀態的不同影像：

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

**影像映射區域的CSS屬性**

影像映射區域的外觀由以下CSS類選擇器控制：

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
   <td colname="col2"> <p>影像映射區域填充顏色。 </p> <p>在中指定此顏色 <span class="codeph"> #RRGGBB </span>。 <span class="codeph"> RGB(R,G,B) </span>或 <span class="codeph"> RGBA(R,G,B,A) </span> 格式 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>影像映射區域填充顏色。 </p> <p>在中指定此顏色 <span class="codeph"> #RRGGBB </span>。 <span class="codeph"> RGB(R,G,B) </span>或 <span class="codeph"> RGBA(R,G,B,A) </span> 格式 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> 影像映射區域邊框樣式。 應指定為「」 <span class="codeph"> 寬度 </span> <span class="codeph"> 純色 </span>」 <span class="codeph"> 寬度 </span> 以像素表示， <span class="codeph"> 顏色 </span> 設定為 <span class="codeph"> #RRGGBB </span>。 <span class="codeph"> RGB(R,G,B) </span>或 <span class="codeph"> RGBA(R,G,B,A) </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定具有一個像素黑色邊框的透明影像映射區域：

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
