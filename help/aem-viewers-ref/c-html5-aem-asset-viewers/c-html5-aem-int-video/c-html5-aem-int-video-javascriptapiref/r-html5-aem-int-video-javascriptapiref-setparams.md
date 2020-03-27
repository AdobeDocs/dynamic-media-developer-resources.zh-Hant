---
description: 互動式視訊檢視器的JavaScript API參考。
seo-description: 互動式視訊檢視器的JavaScript API參考。
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 0a5b9798-0e3f-4310-9b6e-0214a420951b
translation-type: tm+mt
source-git-commit: 94b8dde58cda2670f3e2f22f217599c23601e450

---


# setParams{#setparams}

互動式視訊檢視器的JavaScript API參考。

` setParams( *`params`*)`

將一個或多個參數設定為給定值。 方法引數語法與URL查詢字串相同。 也就是說，它表示與分隔的name=value對 `&`。 與查詢字串一樣，名稱和值使用UTF8進行百分比編碼。 在呼叫之 `init()`前，必須呼叫此參數。

如果檢視器設定資訊是與 `config` JSON物件一起傳遞至建構函式，此方法為選用。

另請參見 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。


## 參數 {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value參數對，與&amp; <span class="codeph"> 分隔</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
