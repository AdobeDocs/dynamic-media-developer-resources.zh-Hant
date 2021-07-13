---
description: Facebook共用工具包含新增至「社交分享」面板的按鈕。 按一下按鈕時，系統會將使用者重新導向至社交服務提供的共用對話方塊。 按鈕的位置由Social分享工具完全管理。
solution: Experience Manager
title: Facebook共用
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,User
exl-id: 0525bfd0-ce38-4fd1-a5cc-e6b5acab1651
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Facebook共用{#facebook-share}

Facebook共用工具包含新增至「社交分享」面板的按鈕。 按一下按鈕時，系統會將使用者重新導向至社交服務提供的共用對話方塊。 按鈕的位置由Social分享工具完全管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

facebook共用按鈕的外觀由下列CSS類別選取器控制：

```
.s7ecatalogviewer .s7facebookshare
```

**facebook共用工具的CSS屬性**

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
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>另請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

您可以在其CSS類別上設定`display:none` CSS屬性，從Social共用面板中移除按鈕。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

範例：若要設定28 x 28像素的Facebook共用按鈕，並針對四個不同按鈕狀態中的每一個顯示不同的影像：

```
.s7ecatalogviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
