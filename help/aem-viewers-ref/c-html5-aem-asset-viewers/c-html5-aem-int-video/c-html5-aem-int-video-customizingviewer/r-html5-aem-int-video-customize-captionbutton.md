---
description: 此按鈕可切換隱藏字幕的顯示和顯示。 如果未指定標題參數，則不會顯示。
seo-description: 此按鈕可切換隱藏字幕的顯示和顯示。 如果未指定標題參數，則不會顯示。
seo-title: 標題按鈕
solution: Experience Manager
title: 標題按鈕
topic: Dynamic media
uuid: a3895a9a-972a-4259-9418-b78f7c904bd4
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Caption button{#caption-button}

此按鈕可切換隱藏字幕的顯示和顯示。 如果未指定標題參數，則不會顯示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

您可以使用CSS，相對於包含此按鈕的控制列來調整此按鈕的大小、外觀和位置。

此按鈕的外觀由下列CSS類別選擇器控制：

```
.s7interactivevideoviewer .s7closedcaptionbutton
```

**標題按鈕的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p> 從上邊框的位置，包括間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p> 從右邊框定位，包括間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p> 從左邊框中的位置，包括間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從底部邊框的位置，包括間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 全螢幕按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>全螢幕按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕狀態的顯示影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 閱CSS精靈 </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕同時支援 `state` 和屬 `selected` 性選擇器，可用來將不同的外觀套用至不同的按鈕狀態。 尤其是， `selected='true'` 對應標題可見時的狀態，以及標 `selected='false'` 題隱藏時的使用狀態。

按鈕工具提示可以本地化。 如需詳 [細資訊，請參閱使用者介面元素](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 的本地化。

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

若要設定28 x 28像素的隱藏字幕按鈕，請從控制列的頂端放置4個像素，從控制列的右邊緣放置68像素，並在選取或未選取時，針對四個不同按鈕狀態中的每個狀態顯示不同的影像。

```
.s7interactivevideoviewer .s7closedcaptionbutton { 
 position:absolute; 
 top:4px; 
 right:68px; 
 width:28px; 
 height:28px; 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='true'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_up.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='true'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='true'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='false'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='false'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='false'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png);  
}
```

