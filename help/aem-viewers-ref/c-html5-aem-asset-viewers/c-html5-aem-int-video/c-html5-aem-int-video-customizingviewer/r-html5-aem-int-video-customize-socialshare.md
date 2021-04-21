---
description: 社交分享工具預設會出現在右上角。 它由按鈕和面板組成，當使用者點按或點選按鈕時，面板會展開，並包含個別的共用工具。
solution: Experience Manager
title: 社交分享
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: ad544a12-d2a4-45c9-9e76-e0bf96901725
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 2%

---

# 社交分享{#social-share}

社交分享工具預設會出現在右上角。 它由按鈕和面板組成，當使用者點按或點選按鈕時，面板會展開，並包含個別的共用工具。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

在檢視器使用者介面中，社交分享工具的位置和大小由下列項目控制：

```
.s7interactivevideoviewer .s7socialshare
```

**社交分享工具的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p> 社交分享工具相對於檢視器容器的垂直位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p> 社交分享工具相對於檢視器容器的水準位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 社交分享工具的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>社交分享工具的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#example}

若要設定社交分享工具，該工具從檢視器容器的頂端放置四個像素，從檢視器容器的右側放置五個像素，大小為28 x 28像素。

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

社交分享工具按鈕的外觀是透過下列CSS類別選取器加以控制：

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton
```

**社交分享工具按鈕的CSS屬性**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p> 為指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用來將不同的外觀套用至不同的按鈕狀態。

按鈕工具提示可以本地化。 請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

## 範例 {#example-1}

若要設定社交分享工具按鈕，針對四個不同的按鈕狀態顯示不同的影像。

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

包含個別社交共用圖示的面板外觀由下列CSS類別選擇器控制：

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel
```

**社交共用面板的CSS屬性**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色  </span> </p> </td> 
   <td colname="col2"> <p>面板的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#example-2}

要設定面板以使其具有透明顏色：

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
