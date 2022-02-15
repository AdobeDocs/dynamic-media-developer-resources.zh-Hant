---
title: 設定資產
description: 視頻查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e5d71393-fcae-4bd4-8e78-a451b2f05ffc
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# 設定資產{#setasset}

視頻查看器的JavaScript API參考。

`setAsset(asset[, data])`

設定新資產和可選附加資產資料。 可以在任何時間（在之前或之後）調用此參數 `init()`。 如果在 `init()`，查看器在運行時交換資產。

另請參閱 [初始化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 參數 {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ 0} <span class="codeph"> 字串 </span>}新資產ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 資料 </span> </p> </td> 
   <td colname="col2"> <p>{ 0} <span class="codeph"> JSON </span>} JSON對象具有以下可選欄位（區分大小寫）: </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 後驗 </span>  — 在視頻開始播放之前，要在第一幀上顯示的影像。 請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.後驗影像 </a>。 </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> 字幕 </span>  — 新隱藏字幕檔案的位置。 如果未指定檔案，則用戶介面中不顯示隱藏的標題按鈕。 </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> 導航 </span> - WebVTT導航內容的URL或路徑。 WebVTT檔案應由影像服務提供 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```
