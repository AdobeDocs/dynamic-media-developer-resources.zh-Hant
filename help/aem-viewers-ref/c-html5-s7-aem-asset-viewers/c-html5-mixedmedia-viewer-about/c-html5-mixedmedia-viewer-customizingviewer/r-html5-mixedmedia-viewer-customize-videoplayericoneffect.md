---
title: 視訊播放器圖示效果
description: 「播放」圖示覆蓋在視訊檢視區域上。 它會在視訊暫停或到達視訊結尾時顯示，也會取決於iconeffect引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
TQID: 'https://experienceleague.adobe.com/LAq8JtRGEkPSrYm5QLGQz6RjhpSSxx7lQcbyaZsIhIw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 0%

---

# 視訊播放器圖示效果{#video-player-icon-effect}

「播放」圖示覆蓋在視訊檢視區域上。 它會在視訊暫停或到達視訊結尾時顯示，也會取決於iconeffect引數。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

使用下列CSS類別選取器來控制播放圖示的外觀：

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

播放圖示的&#x200B;**CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景影像</span> </p> </td> 
   <td colname="col2"> <p> 播放圖示顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS拼寫，則定位在圖稿sprite內。 </p> <p>請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p> 播放圖示的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>播放圖示的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

圖示效果支援`state`屬性選取器。 選取器`state="play"`用於視訊在播放中暫停時，而`state="replay"`用於播放磁頭在資料流結尾時。

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定100 x 100畫素播放圖示。

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
