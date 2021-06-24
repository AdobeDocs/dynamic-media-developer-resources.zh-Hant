---
description: 社交分享工具預設會顯示在右上角。 它包含按鈕和面板，當使用者點按或點選按鈕時會展開，並包含個別的共用工具。
solution: Experience Manager
title: 社交分享
feature: Dynamic Media Classic，檢視器， SDK/API，影片
role: Developer,Business Practitioner
exl-id: 82b482f9-b117-4529-a422-cdb0eead0031
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 1%

---

# 社交分享{#social-share}

社交分享工具預設會顯示在右上角。 它包含按鈕和面板，當使用者點按或點選按鈕時會展開，並包含個別的共用工具。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

檢視器使用者介面中社交分享工具的位置和大小由下列項目控制：

```
.s7videoviewer .s7socialshare
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

範例 — 設定社交分享工具，該工具的大小為28 x 28像素，從頂端放置四個像素，從檢視器容器右側放置五個像素。

```
.s7videoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

社交分享工具按鈕的外觀由下列CSS類別選取器控制：

```
.s7videoviewer .s7socialshare .s7socialbutton
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
   <td colname="col2"> <p> 如果使用CSS精靈，則位於圖稿精靈內。 </p> <p>請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援`state`屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。

按鈕工具提示可以本地化。 如需詳細資訊，請參閱[使用者介面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 。

範例 — 設定社交分享工具按鈕，針對四個不同按鈕狀態中的每一個顯示不同的影像。

```
.s7videoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

包含個別社交分享圖示的面板外觀會由下列CSS類別選取器控制：

```
.s7videoviewer .s7socialshare .s7socialsharepanel
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
.s7videoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
