---
title: 註解按鈕
description: 此按鈕可切換隱藏式字幕顯示開啟和關閉。 如果未指定註解引數，則不會顯示註解引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 47d4a33b-e2bc-4a32-be45-5320d3de1955
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 2%

---

# 註解按鈕{#caption-button}

此按鈕可切換隱藏式字幕顯示開啟和關閉。 如果未指定註解引數，則不會顯示註解引數。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

您可以使用CSS來調整此按鈕的大小、外觀和位置（相對於包含此按鈕的控制列）。

此按鈕的外觀是由下列CSS類別選取器所控制：

```
.s7videoviewer .s7closedcaptionbutton
```

**註解按鈕的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p> 上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p> 從右邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p> 從左邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從下邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 全熒幕按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>全熒幕按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕狀態的顯示影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS拼寫，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕同時支援 `state` 和 `selected` 屬性選取器，可將不同的外觀元素套用至不同的按鈕狀態。 尤其是， `selected='true'` 對應於註解可見時的狀態，並且 `selected='false'` 隱藏註解時使用。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

若要設定隱藏式字幕按鈕，其大小為28 x 28畫素，並從控制列的頂端放置4個畫素，從右邊緣放置68個畫素。 最後，選取或未選取時，針對四種不同按鈕狀態分別顯示不同的影像。

```
.s7videoviewer .s7closedcaptionbutton { 
 position:absolute; 
 top:4px; 
 right:68px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7closedcaptionbutton[selected='true'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_up.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='true'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='true'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='false'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='false'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='false'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png);  
}
```
