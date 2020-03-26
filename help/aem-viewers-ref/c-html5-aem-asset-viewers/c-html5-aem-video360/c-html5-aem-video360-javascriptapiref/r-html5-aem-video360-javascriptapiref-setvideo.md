---
description: Video360檢視器的JavaScript API參考
seo-description: Video360檢視器的JavaScript API參考
seo-title: setVideo
solution: Experience Manager
title: setVideo
topic: Dynamic media
uuid: 749aa32c-c27f-476c-954b-d4524528bccc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setVideo{#setvideo}

Video360檢視器的JavaScript API參考

`setVideo(videoUrl)`

設定新的外部視訊。 可隨時呼叫，不論在前後皆可 `init()`。 如果在之後 `init()`呼叫，檢視器會在執行時期切換視訊。

另請參見 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 參數 {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>}新視訊的絕對URL。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```

