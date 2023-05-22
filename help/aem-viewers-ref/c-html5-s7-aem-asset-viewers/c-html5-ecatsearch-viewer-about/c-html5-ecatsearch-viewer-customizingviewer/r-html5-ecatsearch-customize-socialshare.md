---
title: 社會份額
description: 預設情況下，社交共用工具將出現在左上角。 它由按鈕和面板組成，當用戶按一下或點擊按鈕時，面板將展開，並包含各個共用工具。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5cac6c86-08fb-46fd-bab0-ab77154eb770
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# 社會份額{#social-share}

預設情況下，社交共用工具將出現在左上角。 它由按鈕和面板組成，當用戶按一下或點擊按鈕時，面板將展開，並包含各個共用工具。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

用戶介面中社交共用工具的位置和大小由下列方式控制：

```
.s7ecatalogsearchviewer .s7socialshare
```

**社交共用工具的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上邊距 </span> </p> </td> 
   <td colname="col2"> <p> 從控制欄頂部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 邊距：左 </span> </p> </td> 
   <td colname="col2"> <p> 到左邊的下一個按鈕的距離，如果此按鈕是行中的第一個按鈕，則到控制欄的左側的距離。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 社交共用工具的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>社交共用工具的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定一個社交共用工具，該工具從頂部放置四個像素，從查看器容器右側放置五個像素，大小為28 x 28像素。

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

社交共用工具按鈕的外觀由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
```

**社交按鈕的CSS屬性**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景影像 </span> </p> </td> 
   <td colname="col2"> <p> 為給定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS浮雕，則在圖稿浮雕內定位。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS繁體 </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可用於將不同外觀應用於不同按鈕狀態。

按鈕工具提示可以本地化。 請參閱 [用戶介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 的子菜單。

示例 — 設定一個社交共用工具按鈕，該按鈕顯示四個不同按鈕狀態中每個狀態的不同影像。

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

包含各個社會共用表徵圖的面板的外觀由以下CSS類選擇器控制：

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
```

**社交共用面板的CSS屬性**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>面板的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 設定具有透明顏色的面板：

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
