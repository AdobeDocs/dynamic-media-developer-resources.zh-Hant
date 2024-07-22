---
title: 縮圖按鈕
description: 按一下或點選此按鈕會重設主要檢視與縮圖之間的檢視器。 此按鈕會出現在主控制列中。 您可以使用CSS調整此按鈕的大小、外觀和位置。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: ddd976ca-6043-4930-8ce6-f58fad226ff3
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# 縮圖按鈕{#thumbnails-button}

選取或點選此按鈕會重設主檢視與縮圖之間的檢視器。 此按鈕會出現在主控制列中。 您可以使用CSS調整此按鈕的大小、外觀和位置。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

主要檢視器區域的&#x200B;**CSS屬性**

使用下列CSS類別選取器來控制按鈕的外觀：

`.s7ecatalogviewer .s7thumbnailpagebutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上邊界</span> </p> </td> 
   <td colname="col2"> <p> 從控制列頂端的位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">左邊界</span> </p> </td> 
   <td colname="col2"> <p> 與左側或控制列左側的下一個按鈕的距離（若是列中的第一個按鈕）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景影像</span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS拼寫，則定位在圖稿sprite內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕同時支援`state`和`selected`屬性選取器，它們可用來將不同的外觀元素套用至不同的按鈕狀態。 特別是，`selected='true'`對應於縮圖模式為作用中狀態的檢視器狀態，而`selected='false'`對應於主檢視的預設狀態。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

範例 — 設定縮圖按鈕，其大小為28 x 28畫素，且位於距底部4畫素、距主控列左邊緣5畫素的位置。 最後，選取或未選取時，針對四種不同按鈕狀態分別顯示不同的影像。

```
.s7ecatalogviewer .s7thumbnailpagebutton{ 
margin-top: 4px; 
margin-left: 5px; width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='up'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='over'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='down'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='disabled'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='up'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='over'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='down'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='disabled'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_disabled.png); 
}
```
