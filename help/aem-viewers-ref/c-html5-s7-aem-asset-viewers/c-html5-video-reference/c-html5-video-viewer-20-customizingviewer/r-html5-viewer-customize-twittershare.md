---
description: Twitter分享工具包含新增至Social分享面板的按鈕。 按一下按鈕時，使用者會重新導向至社交服務所提供的分享對話方塊。 按鈕的位置由Social分享工具完全管理。
seo-description: Twitter分享工具包含新增至Social分享面板的按鈕。 按一下按鈕時，使用者會重新導向至社交服務所提供的分享對話方塊。 按鈕的位置由Social分享工具完全管理。
seo-title: Twitter分享
solution: Experience Manager
title: Twitter分享
topic: Dynamic Media
uuid: 15fed20e-89c4-4c4b-8f0d-1f0bac0c0af7
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---


# Twitter分享{#twitter-share}

Twitter分享工具包含新增至Social分享面板的按鈕。 按一下按鈕時，使用者會重新導向至社交服務所提供的分享對話方塊。 按鈕的位置由Social分享工具完全管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

使用下列CSS類別選擇器來控制Twitter分享按鈕的外觀：

```
.s7videoviewer .s7twittershare
```

**Twitter共用工具的CSS屬性**

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
   <td colname="col1"> <p> <span class="codeph"> 背景影像  </span> </p> </td> 
   <td colname="col2"> <p> 為指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用來將不同的外觀套用至不同的按鈕狀態。

您可在Social共用面板的CSS類別上設定`display:none` CSS屬性，以移除該按鈕。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)。

範例——若要設定28 x 28像素的Twitter分享按鈕，並針對四個不同的按鈕狀態顯示不同的影像：

```
.s7videoviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7videoviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7videoviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7videoviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```

