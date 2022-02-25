---
title: 全屏按鈕
description: 使查看器在用戶按一下時進入或退出全屏模式。 如果查看器在彈出模式下工作，且系統不支援本機全屏，則此按鈕不顯示。 可以使用CSS調整此按鈕的大小、外觀和位置。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ec8ebf24-c8ae-43f1-86b9-0b30d529d277
source-git-commit: d5f1f05c36c1cb8a57b5a4bb8a9d066c20e32e75
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 2%

---

# 全屏按鈕{#full-screen-button}

當用戶選擇時，使查看器進入或退出全屏模式。 如果查看器在彈出模式下工作，且系統不支援本機全屏，則此按鈕不顯示。 可以使用CSS調整此按鈕的大小、外觀和位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器區域的CSS屬性**

按鈕的外觀由以下CSS類選擇器控制：

```
.s7basiczoomviewer .s7fullscreenbutton
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>從上邊框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p>從右邊框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左側 </span> </p> </td> 
   <td colname="col2"> <p>從左邊框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從底邊框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p>為給定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS浮雕，則在圖稿浮雕內定位。 </p> <p>請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-customizingviewer/c-html5-20-basic-zoom-viewer-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS繁體 </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 和 `selected` 屬性選擇器，可用於將不同的外觀應用於不同的按鈕狀態。 特別是， `selected='true'` 對應於「全屏」狀態 `selected='false'` 對應於「正常」狀態。

按鈕工具提示可以本地化。 請參閱 [用戶介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 的子菜單。

示例 — 設定一個32 x 32像素的全屏按鈕，並從查看器的上邊緣和右邊緣放置6個像素。 當選定或未選定時，它必須為四個不同按鈕狀態中的每個狀態顯示不同的影像：

```
.s7basiczoomviewer .s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7basiczoomviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7basiczoomviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7basiczoomviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7basiczoomviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7basiczoomviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7basiczoomviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7basiczoomviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7basiczoomviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
