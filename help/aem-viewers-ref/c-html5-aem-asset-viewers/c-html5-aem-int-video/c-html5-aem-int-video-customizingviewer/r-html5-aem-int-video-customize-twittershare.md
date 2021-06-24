---
description: Twitter共用工具包含新增至「社交分享」面板的按鈕。 按一下按鈕時，系統會將使用者重新導向至社交服務提供的共用對話方塊。 按鈕的位置由Social分享工具完全管理。
solution: Experience Manager
title: Twitter共用
feature: Dynamic Media Classic，檢視器， SDK/API，互動式影片
role: Developer,Business Practitioner
exl-id: 045ca718-b971-4437-a0bf-580eee83ff2d
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# Twitter共用{#twitter-share}

Twitter共用工具包含新增至「社交分享」面板的按鈕。 按一下按鈕時，系統會將使用者重新導向至社交服務提供的共用對話方塊。 按鈕的位置由Social分享工具完全管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

twitter共用按鈕的外觀由下列CSS類別選取器控制：

```
.s7interactivevideoviewer .s7twittershare
```

**twitter共用工具的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像  </span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

您可以在其CSS類別上設定`display:none` CSS屬性，從Social共用面板中移除按鈕。

按鈕工具提示可以本地化。 請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

## 範例 {#section-5a8837ea208e48ed8dfa6a3c1a514492}

若要設定28 x 28像素的Twitter共用按鈕，並針對四個不同按鈕狀態中的每個狀態顯示不同的影像：

```
.s7interactivevideoviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7interactivevideoviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
