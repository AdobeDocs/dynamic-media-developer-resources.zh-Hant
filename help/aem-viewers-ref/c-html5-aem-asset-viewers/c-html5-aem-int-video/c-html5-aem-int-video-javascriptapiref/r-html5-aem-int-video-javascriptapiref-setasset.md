---
description: 互動式視訊檢視器的JavaScript API參考。
seo-description: 互動式視訊檢視器的JavaScript API參考。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 80c670a4-1251-47f5-a66b-8ba5019df1ce
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# setAsset{#setasset}

互動式視訊檢視器的JavaScript API參考。

`setAsset(asset[, data])`

設定新資產和可選的其他資產資料。 您可以隨時呼叫此參數，不論是在之前或之後 `init()`。 如果在之後呼叫，檢 `init()`視器會在執行時期交換資產。

另請參見 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>}新資產ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 資料 </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> JSON} </span>JSON物件及下列選填欄位（區分大小寫）: </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> 後驗 </span> 影像——在視訊開始播放之前，要在第一個影格上顯示的影像。 請參 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> 閱VideoPlayer.postemage </a>。 </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> 標題 </span> -新標題檔案的位置。 如果未指定，標題按鈕在使用者介面中不可見。 </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> navigation </span> - WebVTT導覽內容的URL或路徑。 WebVTT檔案應由影像伺服提供。 </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interactiveData </span> - WebVTT互動資料內容的URL或路徑。 WebVTT檔案必須由影像伺服提供。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```

