---
title: twitter共用
description: twitter共用工具包含新增至「社交」共用面板的按鈕。 選取按鈕時，使用者會重新導向至社交服務提供者的共用對話方塊。 按鈕的位置可完全由社交分享工具管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 045ca718-b971-4437-a0bf-580eee83ff2d
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# twitter共用{#twitter-share}

twitter共用工具包含新增至「社交」共用面板的按鈕。 選取按鈕時，使用者會重新導向至社交服務提供者的共用對話方塊。 按鈕的位置可完全由社交分享工具管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

twitter共用按鈕的外觀是由下列CSS類別選取器所控制：

```
.s7interactivevideoviewer .s7twittershare
```

twitter共用工具的&#x200B;**CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景影像</span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS拼寫，則定位在圖稿sprite內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選取器，可用來將不同的外觀元素套用至不同的按鈕狀態。

您可以在其CSS類別上設定`display:none` CSS屬性，以從Social共用面板移除按鈕。

按鈕工具提示可以本地化。 請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

## 範例 {#section-5a8837ea208e48ed8dfa6a3c1a514492}

若要設定28 x 28畫素的Twitter共用按鈕，並針對四種不同按鈕狀態分別顯示不同的影像：

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
