---
description: 社交分享工具預設會顯示在左上角。 它包含按鈕和面板，當使用者點按或點選按鈕時會展開，並包含個別的共用工具。
solution: Experience Manager
title: 社交分享
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog
role: Developer,User
exl-id: b65b8846-3287-47ae-bdb6-6cac768cece0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 社交分享{#social-share}

社交分享工具預設會顯示在左上角。 它包含按鈕和面板，當使用者點按或點選按鈕時會展開，並包含個別的共用工具。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

檢視器使用者介面中社交分享工具的位置和大小由下列項目控制：

```
.s7ecatalogviewer .s7socialshare
```

**社交分享工具的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距上  </span> </p> </td> 
   <td colname="col2"> <p> 從控制欄頂端的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left  </span> </p> </td> 
   <td colname="col2"> <p> 左側的下一個按鈕的距離；如果這是行中的第一個按鈕，則控制欄的左側。 </p> </td> 
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

範例 — 設定社交分享工具，該工具的大小為28 x 28像素，從頂端放置四個像素，從檢視器容器右側放置五個像素。

```
.s7ecatalogviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

社交分享工具按鈕的外觀由下列CSS類別選取器控制：

```
.s7ecatalogviewer .s7socialshare .s7socialbutton
```

**社交按鈕的CSS屬性**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
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

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

範例 — 設定社交分享工具按鈕，針對四個不同按鈕狀態中的每一個顯示不同的影像。

```
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

包含個別社交分享圖示的面板外觀會由下列CSS類別選取器控制：

```
.s7ecatalogviewer .s7socialshare .s7socialsharepanel
```

**社交分享面板的CSS屬性**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色  </span> </p> </td> 
   <td colname="col2"> <p>面板的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定面板以使用透明顏色：

```
.s7ecatalogviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
