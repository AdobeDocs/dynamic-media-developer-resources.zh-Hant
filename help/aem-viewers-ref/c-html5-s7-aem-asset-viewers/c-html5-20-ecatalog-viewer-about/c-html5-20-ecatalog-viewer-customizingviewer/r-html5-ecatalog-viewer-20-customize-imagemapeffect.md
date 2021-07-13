---
description: 根據mode參數的值，在原本以Dynamic Media Classic製作地圖的地方，檢視器會在主檢視上顯示影像地圖圖示，或轉譯與原始影像地圖形狀相符的確切區域。
solution: Experience Manager
title: 影像地圖效果
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,User
exl-id: 3816118f-4eb7-4436-9f54-155dde077734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%

---

# 影像地圖效果{#image-map-effect}

根據mode參數的值，在原本以Dynamic Media Classic製作地圖的地方，檢視器會在主檢視上顯示影像地圖圖示，或轉譯與原始影像地圖形狀相符的確切區域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

影像地圖圖示的外觀由下列CSS類別選取器控制：

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>過去用來設定影像地圖圖示樣式的`s7mapoverlay` CSS類別現已過時；請改用`s7icon`。

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p>影像地圖表徵圖圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>影像地圖圖示寬度（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>影像地圖圖示高度（像素）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>影像映射表徵圖支援`state`屬性選擇器，可用於將不同的外觀應用於`default`和`active`的表徵圖狀態。

範例：設定28 x 28像素的影像地圖圖示，以針對兩個不同圖示狀態中的每一個顯示不同影像。

```
.s7ecatalogviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

另請參閱[影像映射支援](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)。

影像映射區域的外觀由以下CSS類選擇器控制：

```
.s7ecatalogviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景  </span> </p> </td> 
   <td colname="col2"> <p> 影像映射區域填充顏色。 </p> <p>在#RRGGBB、RGB(R、G、B)或RGBA(R、G、B、A)格式中指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 影像映射區域填充顏色。 </p> <p>在#RRGGBB、RGB(R、G、B)或RGBA(R、G、B、A)格式中指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> 影像映射區域邊框樣式。 </p> <p>指定為<span class="codeph"> <span class="varname">寬度</span>實心<span class="varname">顏色</span> </span>，其中<span class="codeph"> <span class="varname">寬度</span> </span>以像素表示，並且<span class="codeph"> <span class="varname">顏色</span> </span>設定為#RRGGBB、RGB(R,G,B)或RBA(R,B,A)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 使用`1`像素黑色邊框設定透明影像映射區域：

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
