---
title: 表徵圖效果
description: 縮放指示器重疊在主視區上。 當影像處於重置狀態時，會顯示它，並且它還取決於影像效果參數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: fee22d02-172c-4f82-9b6c-e06db530f400
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---

# 表徵圖效果{#icon-effect}

縮放指示器重疊在主視區上。 當影像處於重置狀態時，會顯示它，並且它還取決於影像效果參數。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

查看區域的外觀由以下CSS類選擇器控制：

```
.s7ecatalogviewer .s7pageview .s7iconeffect
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
   <td colname="col2"> <p> 縮放指示器圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS浮雕，則在圖稿浮雕內定位。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS繁體 </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮放指示器寬度（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮放指示器高度（以像素為單位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>表徵圖效果支援 `media-type` 屬性選擇器，您可以使用該選擇器對不同設備應用不同的表徵圖效果。 特別是， `media-type='standard'` 對應於通常使用滑鼠輸入的案頭系統 `media-type='multitouch'` 與具有觸摸輸入的設備相對應。

示例 — 為台式機系統和觸摸設備設定100 x 100像素縮放指示器，採用不同的技術。

```
.s7ecatalogviewer .s7pageview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
