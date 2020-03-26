---
description: Facebook分享工具包含新增至Social分享面板的按鈕。 按一下按鈕時，使用者會重新導向至社交服務所提供的分享對話方塊。 按鈕的位置由Social分享工具完全管理。
seo-description: Facebook分享工具包含新增至Social分享面板的按鈕。 按一下按鈕時，使用者會重新導向至社交服務所提供的分享對話方塊。 按鈕的位置由Social分享工具完全管理。
seo-title: Facebook分享
solution: Experience Manager
title: Facebook分享
topic: Dynamic media
uuid: 1b79ad43-7fdf-4046-a225-1f585ff839b6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Facebook分享{#facebook-share}

Facebook分享工具包含新增至Social分享面板的按鈕。 按一下按鈕時，使用者會重新導向至社交服務所提供的分享對話方塊。 按鈕的位置由Social分享工具完全管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Facebook分享按鈕的外觀是使用下列CSS類別選擇器來控制：

```
.s7ecatalogsearchviewer .s7facebookshare
```

**Facebook共用工具的CSS屬性**

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
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p> 為指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS精靈，請放在圖稿精靈內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈 </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援屬 `state` 性選擇器，可用來將不同的外觀套用至不同的按鈕狀態。

您可以在Social共用面板的CSS類別上設定 `display:none` CSS屬性，以移除該按鈕。

按鈕工具提示可以本地化。 如需詳 [細資訊，請參閱使用者介面元素](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 的本地化。

範例——若要設定28 x 28像素的Facebook分享按鈕，並針對四個不同的按鈕狀態顯示不同的影像：

```
.s7ecatalogsearchviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```

