---
title: facebook共用
description: facebook共用工具包含新增至「社交共用」面板的按鈕。 選取按鈕時，使用者會重新導向至社交服務提供者的共用對話方塊。 按鈕的位置可完全由社交分享工具管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: e6ec2cd8-7b2e-4b3c-851d-1a4bbecd4d65
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# facebook共用{#facebook-share}

facebook共用工具包含新增至「社交共用」面板的按鈕。 選取按鈕時，使用者會重新導向至社交服務提供者的共用對話方塊。 按鈕的位置可完全由社交分享工具管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

facebook共用按鈕的外觀是由下列CSS類別選取器所控制：

```
.s7smartcropvideoviewer .s7facebookshare
```

facebook共用工具的&#x200B;**CSS屬性**

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
   <td colname="col2"> <p> 若使用CSS拼寫，則定位在圖稿sprite內。 </p> <p>請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選取器，可用來將不同的外觀元素套用至不同的按鈕狀態。

您可以在其CSS類別上設定`display:none` CSS屬性，以從Social共用面板移除按鈕。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)。

範例 — 設定28 x 28畫素的Facebook共用按鈕，並針對四種不同按鈕狀態分別顯示不同影像：

```
.s7smartcropvideoviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
