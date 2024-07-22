---
title: 影像地圖效果
description: 根據mode引數的值，檢視器會在地圖原本是在Dynamic Media Classic中製作的位置的主檢視上顯示影像地圖圖示，或呈現符合原始影像地圖形狀的精確區域。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 873fc387-1d2a-4d74-b85e-fcbb13b691c5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# 影像地圖效果{#image-map-effect}

根據mode引數的值，檢視器會在地圖原本是在Dynamic Media Classic中製作的位置的主檢視上顯示影像地圖圖示，或呈現符合原始影像地圖形狀的精確區域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主要檢視器區域的&#x200B;**CSS屬性**

影像地圖圖示的外觀是由下列CSS類別選取器所控制：

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>過去用來設定影像地圖圖示樣式的`s7mapoverlay` CSS類別現已棄用；請改用`s7icon`。

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景影像</span> </p> </td> 
   <td colname="col2"> <p>影像地圖圖示圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS拼寫，則定位在圖稿sprite內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>影像地圖圖示寬度（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>影像地圖圖示高度（畫素）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>影像地圖圖示支援`state`屬性選取器，可用來將不同的外觀元素套用至`default`和`active`的圖示狀態。

範例 — 設定28 x 28畫素的影像地圖圖示，針對兩種不同的圖示狀態分別顯示不同的影像。

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

影像地圖區域的外觀是由下列CSS類別選取器所控制：

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
   <td colname="col1"> <p> <span class="codeph">背景</span> </p> </td> 
   <td colname="col2"> <p> 影像地圖區域填滿色彩。 </p> <p>以#RRGGBB、RGB(R，G，B)或RGBA(R，G，B，A)格式指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p> 影像地圖區域填滿色彩。 </p> <p>以#RRGGBB、RGB(R，G，B)或RGBA(R，G，B，A)格式指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">邊框</span> </p> </td> 
   <td colname="col2"> <p> 影像地圖區域框線樣式。 </p> <p>指定為<span class="codeph"> <span class="varname">寬度</span>純色<span class="varname">色彩</span> </span>，其中<span class="codeph"> <span class="varname">寬度</span> </span>是以畫素表示，而<span class="codeph"> <span class="varname">色彩</span> </span>設定為#RRGGBB、RGB(R，G，B)或RGBA(R，G，B，A)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定具有`1`畫素黑色邊框的透明影像地圖區域：

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
