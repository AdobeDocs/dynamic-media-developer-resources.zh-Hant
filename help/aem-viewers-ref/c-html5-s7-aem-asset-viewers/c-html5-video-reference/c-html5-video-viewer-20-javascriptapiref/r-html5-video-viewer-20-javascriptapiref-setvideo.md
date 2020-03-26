---
description: 視訊檢視器的JavaScript API參考
seo-description: 視訊檢視器的JavaScript API參考
seo-title: setVideo
solution: Experience Manager
title: setVideo
topic: Dynamic media
uuid: 0a1b3caa-ded6-4020-962c-41c3ece0a865
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setVideo{#setvideo}

視訊檢視器的JavaScript API參考

`setVideo(videoUrl[, data])`

設定新的外部視訊和選用的其他視訊資料。 可隨時呼叫，不論在前後皆可 `init()`。 如果在之後 `init()`呼叫，檢視器會在執行時期切換視訊。

另請參見 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 參數 {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>}是新視訊的絕對URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 資料 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON} </span>JSON物件及下列選填欄位（區分大小寫）: </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 後驗 </span> 影像——在視訊開始播放之前，要在第一個影格上顯示的影像。 請參 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> 閱VideoPlayer.postemage </a>。 </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> 標題 </span> -新標題檔案的位置。 如果未指定標題檔案，則標題按鈕不會顯示在用戶介面中。 </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> navigation </span> - WebVTT導覽內容的URL或路徑。 WebVTT檔案應由影像伺服提供。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```

