---
description: 縮放指示器覆蓋在縮放視圖區域上。 當影像處於重設狀態時，就會顯示它，而且它也取決於iconeffect參數。
seo-description: 縮放指示器覆蓋在縮放視圖區域上。 當影像處於重設狀態時，就會顯示它，而且它也取決於iconeffect參數。
seo-title: 縮放檢視圖示效果
solution: Experience Manager
title: 縮放檢視圖示效果
topic: Dynamic media
uuid: 69a44789-9587-4459-9c75-048773c9e368
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 縮放檢視圖示效果{#zoom-view-icon-effect}

縮放指示器覆蓋在縮放視圖區域上。 當影像處於重設狀態時，就會顯示它，而且它也取決於iconeffect參數。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主檢視器區域的CSS屬性**

檢視區域的外觀會使用下列CSS類別選擇器加以控制：

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect
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
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> 閱CSS精靈 </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮放指示器寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮放指示器高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>圖示效果支援屬 `media-type` 性選擇器，您可使用它對不同裝置套用不同的圖示效果。 特別地， `media-type='standard'` 對應於通常使用滑鼠輸入的案頭系統，並 `media-type='multitouch'` 對應於具有觸摸輸入的設備。

範例——針對桌上型電腦系統和觸控裝置設定100 x 100像素縮放指示器，並使用不同的圖稿。

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```

