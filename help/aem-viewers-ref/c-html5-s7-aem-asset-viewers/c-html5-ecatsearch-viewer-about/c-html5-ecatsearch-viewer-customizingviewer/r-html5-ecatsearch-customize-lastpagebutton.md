---
title: 「最後一頁」按鈕
description: 選取此按鈕會將使用者導向到目錄中的最後一頁。 此按鈕會顯示在桌上型電腦系統和平板電腦上的主要控制列中；在行動電話上，此按鈕會新增至次要控制列。 您可以使用CSS調整此按鈕的大小、外觀和位置。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa1ff52c-6fb1-47e7-b3d4-216fea02bbd8
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 2%

---

# 「最後一頁」按鈕{#last-page-button}

選取此按鈕會將使用者導向到目錄中的最後一頁。 此按鈕會顯示在桌上型電腦系統和平板電腦上的主要控制列中；在行動電話上，此按鈕會新增至次要控制列。 您可以使用CSS調整此按鈕的大小、外觀和位置。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**主要檢視器區域的CSS屬性**

按鈕的外觀由下列CSS類別選取器控制：

`.s7ecatalogsearchviewer .s7lastpagebutton .s7panleftbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>從主要控制列（在桌上型電腦系統和平板電腦上）或次要控制列（在行動電話上）的頂端邊框定位，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p>從主要控制列（在桌上型電腦系統和平板電腦上）或次要控制列（在行動電話上）的右邊框定位，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p>從主要控制列（在桌上型電腦系統和平板電腦上）或次要控制列（在行動電話上）的左邊框定位，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從主要控制列（在桌上型電腦系統和平板電腦上）或次要控制列（在行動電話上）的底部邊框定位，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 以取得詳細資訊。

範例 — 設定最後一個頁面按鈕，其大小為28 x 28畫素，位置為從底部算起4畫素，從主控列的左邊緣算起220畫素。 最後，針對四種不同按鈕狀態分別顯示不同的影像。

```
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton { 
bottom:4px; 
right:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/LastPageButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/LastPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/LastPageButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/LastPageButton_dark_disabled.png); 
}
```
