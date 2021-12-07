---
title: Twitter共用
description: Twitter共用工具包含新增至「社交分享」面板的按鈕。 當選取按鈕時，會將使用者重新導向至社交服務提供的共用對話方塊。 按鈕的位置由Social分享工具完全管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Twitter共用{#twitter-share}

Twitter共用工具包含新增至「社交分享」面板的按鈕。 當選取按鈕時，會將使用者重新導向至社交服務提供的共用對話方塊。 按鈕的位置由Social分享工具完全管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

twitter共用按鈕的外觀由下列CSS類別選取器控制：

```
.s7smartcropvideoviewer .s7twittershare
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
   <td colname="col1"> <p> <span class="codeph"> 背景 — 影像 </span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選取器，可用來將不同的外觀套用至不同的按鈕狀態。

您可以透過設定 `display:none` 其CSS類上的CSS屬性。

按鈕工具提示可以本地化。 請參閱 [用戶介面元素本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得更多資訊。

範例：若要設定28 x 28像素的Twitter共用按鈕，並針對四個不同按鈕狀態中的每一個顯示不同的影像：

```
.s7smartcropvideoviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
