---
title: 影像映射效果
description: 根據模式參數的值，查看器在地圖最初創作於Dynamic Media Classic的地方主視圖上顯示影像映射表徵圖。 或者，它會呈現與原始影像映射的形狀匹配的精確區域。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3816118f-4eb7-4436-9f54-155dde077734
source-git-commit: 6087b48b898e93e605c3873cbd5132b74d04225f
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 1%

---

# 影像映射效果{#image-map-effect}

根據模式參數的值，查看器在地圖最初創作於Dynamic Media Classic的地方主視圖上顯示影像映射表徵圖。 或者，它會呈現與原始影像映射的形狀匹配的精確區域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

影像映射表徵圖的外觀由以下CSS類選擇器控制：

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>的 `s7mapoverlay` 過去用於樣式影像映射表徵圖的CSS類現在已棄用；使用 `s7icon` 的雙曲餘切值。

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
   <td colname="col2"> <p>影像映射表徵圖圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS浮雕，則在圖稿浮雕內定位。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS繁體 </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>影像映射表徵圖寬度（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>影像映射表徵圖高度（以像素為單位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>影像映射表徵圖支援 `state` 屬性選擇器，可用於將不同的外觀應用於 `default` 和 `active`。

示例 — 設定28 x 28像素影像映射表徵圖，該表徵圖顯示兩個不同表徵圖狀態中每個狀態的不同影像。

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

另請參閱 [影像映射支援](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)。

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
   <td colname="col1"> <p> <span class="codeph"> 背景 </span> </p> </td> 
   <td colname="col2"> <p> 影像映射區域填充顏色。 </p> <p>以#RRGGBB、RGB(R,G,B)或RGBA(R,G,B,A)格式指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 影像映射區域填充顏色。 </p> <p>以#RRGGBB、RGB(R,G,B)或RGBA(R,G,B,A)格式指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> 影像映射區域邊框樣式。 </p> <p>指定為 <span class="codeph"> <span class="varname"> 寬度 </span> 堅固 <span class="varname"> 顏色 </span> </span>，也請參見Wiki頁。 <span class="codeph"> <span class="varname"> 寬度 </span> </span> 以像素和 <span class="codeph"> <span class="varname"> 顏色 </span> </span> 設定為#RRGGBB、RGB(R,G,B)或RGBA(R,G,B,A)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定透明影像映射區域 `1` 像素黑色邊框：

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
