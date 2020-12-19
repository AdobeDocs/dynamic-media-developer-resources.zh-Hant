---
description: 視訊檢視器的JavaScript API參考。
seo-description: 視訊檢視器的JavaScript API參考。
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 0497ae9c-e94a-458d-a4c7-5915add17f60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# setParams{#setparams}

視訊檢視器的JavaScript API參考。

` setParams( *`params`*)`

將一個或多個參數設定為給定值。 方法引數語法與URL查詢字串相同。 即，它表示與`&`分隔的name=value對。 名稱和值與查詢字串相同，是使用UTF8進行百分比編碼。 在呼叫`init()`之前，必須呼叫此參數。

如果檢視器設定資訊與`config` JSON物件一起傳遞至建構函式，此方法為選用。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

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

