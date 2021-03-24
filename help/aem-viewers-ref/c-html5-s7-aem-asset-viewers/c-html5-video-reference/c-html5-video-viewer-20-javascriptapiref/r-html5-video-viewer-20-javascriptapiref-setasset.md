---
description: 視訊檢視器的JavaScript API參考。
solution: Experience Manager
title: setAsset
feature: Dynamic Media經典，檢視器，SDK/API，視訊
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---


# setAsset{#setasset}

視訊檢視器的JavaScript API參考。

`setAsset(asset[, data])`

設定新資產和可選的其他資產資料。 您可以隨時在`init()`之前或之後呼叫此參數。 如果在`init()`之後呼叫，檢視器會在執行時期交換資產。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 參數 {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph">字串</span>}新資產ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 資料 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSON物件，包含下列選填欄位（區分大小寫）: </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 後驗 </span> 影像——在視訊開始播放之前，在第一個影格上顯示的影像。請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.pheormage </a>。 </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> 標題 </span> -新隱藏標題檔案的位置。如果未指定檔案，則使用者介面中不會顯示隱藏字幕按鈕。 </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> navigation  </span> - WebVTT導覽內容的URL或路徑。WebVTT檔案應由影像伺服提供 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```

