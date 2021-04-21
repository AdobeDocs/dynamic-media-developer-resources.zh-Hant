---
description: 互動式視訊檢視器的JavaScript API參考。
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 32d26999-7815-4c71-ad4c-b7db99ec3d3b
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# setParams{#setparams}

互動式視訊檢視器的JavaScript API參考。

` setParams( *`params`*)`

將一個或多個參數設定為給定值。 方法引數語法與URL查詢字串相同。 即，它表示與`&`分隔的name=value對。 與查詢字串一樣，名稱和值使用UTF8進行百分比編碼。 在呼叫`init()`之前，必須呼叫此參數。

如果檢視器設定資訊與`config` JSON物件一起傳遞給建構函式，此方法是選用的。

另請參閱[init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。


## 參數 {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value參數對與&amp;分 <span class="codeph"> 隔</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
