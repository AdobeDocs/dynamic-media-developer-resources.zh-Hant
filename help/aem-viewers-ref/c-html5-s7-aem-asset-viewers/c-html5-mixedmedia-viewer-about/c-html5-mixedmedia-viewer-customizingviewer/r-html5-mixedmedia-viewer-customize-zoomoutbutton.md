---
title: 縮小顯示按鈕
description: 按一下或點選此按鈕可縮小主檢視中的影像。 為了節省熒幕空間，此按鈕不會顯示在行動電話上。 您可以使用CSS調整此按鈕的大小、外觀和位置。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3e464e02-bcff-4ddc-b47c-84d0eee7f779
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 2%

---

# 縮小顯示按鈕{#zoom-out-button}

選取此按鈕可縮小主檢視中的影像。 為了節省熒幕空間，此按鈕不會顯示在行動電話上。 您可以使用CSS調整此按鈕的大小、外觀和位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

按鈕的外觀由下列CSS類別選取器控制：

```
.s7mixedmediaviewer .s7zoomoutbutton
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
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p>從右邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p>從左邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從下邊框定位，包括內距。 </p> </td> 
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
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) 以取得詳細資訊。

範例 — 設定縮小顯示按鈕，其大小為32 x 32畫素，位置為檢視器上緣和右緣的6個畫素。 最後，針對四種不同按鈕狀態分別顯示不同的影像。

```
.s7mixedmediaviewer .s7zoomoutbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='up'] { 
background-image:url(images/v2/ZoomOutButton_dark_up.png); 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='over'] {  
background-image:url(images/v2/ZoomOutButton_dark_over.png); 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='down'] {  
background-image:url(images/v2/ZoomOutButton_dark_down.png); 
} 
.s7mixedmediaviewer .s7zoomoutbutton [state='disabled'] { 
background-image:url(images/v2/ZoomOutButton_dark_disabled.png); 
}
```
