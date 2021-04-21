---
description: 視模式參數的值而定，檢視器會在主檢視上顯示影像地圖圖示，而主檢視的地圖原本是在Dynamic Media經典中製作，或轉譯與原始影像地圖形狀相符的精確區域。
solution: Experience Manager
title: 影像地圖效果
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---


# 影像地圖效果{#image-map-effect}

視模式參數的值而定，檢視器會在主檢視上顯示影像地圖圖示，而主檢視的地圖原本是在Dynamic Media經典中製作，或轉譯與原始影像地圖形狀相符的精確區域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

影像地圖圖示的外觀是由下列CSS類別選擇器所控制：

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>過去用來設定影像地圖圖示樣式的`s7mapoverlay` CSS類別現在已不再使用；請改用`s7icon`。

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
   <td colname="col2"> <p>影像地圖圖示圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>影像地圖圖示寬度（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>影像地圖圖示高度（以像素為單位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>影像地圖圖示支援`state`屬性選擇器，您可使用它將不同的外觀套用至`default`和`active`的圖示狀態。

範例——設定28 x 28像素的影像地圖圖示，可針對兩個不同的圖示狀態顯示不同的影像。

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

另請參閱[影像地圖支援](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)。

使用下列CSS類別選取器來控制影像地圖區域的外觀：

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
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
   <td colname="col2"> <p> 影像地圖區域填滿顏色。 </p> <p>在#RRGGBB、RGB(R,G,B)或RGBA(R,G,B,A)格式中指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p> 影像地圖區域填滿顏色。 </p> <p>在#RRGGBB、RGB(R,G,B)或RGBA(R,G,B,A)格式中指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> 影像地圖區域邊框樣式。 </p> <p>指定為<span class="codeph"> <span class="varname">寬度</span>實色<span class="varname"></span>，其中<span class="codeph"> <span class="varname">寬度</span> </span>以像素表示，並將<span class="codeph">顏色</span> </span>設定為#RRGGBB、RGB(R,G,B)或RGBA(R,G,B,A)。</span><span class="varname"> </span></p> </td> 
  </tr> 
 </tbody> 
</table>

範例——使用`1`像素黑色邊框設定透明影像地圖區域：

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

