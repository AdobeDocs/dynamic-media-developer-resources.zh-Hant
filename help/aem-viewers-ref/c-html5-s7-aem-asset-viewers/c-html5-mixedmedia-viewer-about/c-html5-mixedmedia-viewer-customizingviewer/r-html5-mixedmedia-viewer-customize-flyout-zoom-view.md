---
description: 在內聯縮放模式中，主視圖由靜態影像、彈出視圖中顯示的縮放影像和顯示在靜態影像頂部的提示消息組成。
solution: Experience Manager
title: 彈出縮放檢視
feature: Dynamic Media Classic，檢視器，SDK/API，混合媒體集
role: Developer,User
exl-id: 46c91d1f-5809-4270-a06d-5068d20a6341
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 5%

---

# 彈出縮放檢視{#flyout-zoom-view}

在內聯縮放模式中，主視圖由靜態影像、彈出視圖中顯示的縮放影像和顯示在靜態影像頂部的提示消息組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

主要檢視的外觀由下列CSS類別選取器控制：

```
.s7mixedmediaviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p> 主視圖的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要讓主檢視透明：

```
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

提示訊息的外觀由下列CSS類別選取器控制：

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

您可以透過CSS來設定字型樣式、大小外觀和垂直偏移。 不過，水準對齊方式是由檢視器邏輯管理。 不支援使用`left`或`right`屬性透過CSS覆寫它。

**提示訊息的CSS屬性**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>訊息背景填色顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊框半徑  </span> </p> </td> 
   <td colname="col2"> <p> 訊息背景邊框半徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 從主視圖底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>提示文字顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小  </span> </p> </td> 
   <td colname="col2"> <p>字型大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列  </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度  </span> </p> </td> 
   <td colname="col2"> <p> 消息背景不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填補 </span> </p> </td> 
   <td colname="col2"> <p> 在訊息文字周圍填補。 </p> </td> 
  </tr> 
 </tbody> 
</table>

提示訊息可本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) 。

示例 — 要設定半透明的尖端消息，其字型為白色Arial 12px，距主視圖底部50像素偏移，邊框間距和圓角：

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
