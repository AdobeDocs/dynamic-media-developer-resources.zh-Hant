---
description: 視訊檢視器的JavaScript API參考。
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic，檢視器， SDK/API，影片
role: Developer,User
exl-id: 76bad894-bfb8-4d79-b3ff-c2497c68e5e8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---

# setParams{#setparams}

視訊檢視器的JavaScript API參考。

` setParams( *`params`*)`

將一或多個參數設為指定值。 方法引數語法與URL查詢字串相同。 也就是說，它表示以`&`分隔的名稱=值配對。 與查詢字串中相同，名稱和值是使用UTF8進行百分比編碼。 呼叫`init()`之前，必須呼叫此參數。

如果將檢視器配置資訊與`config` JSON物件傳遞至建構函式，則此方法為選用。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value參數對(以&amp; <span class="codeph"> 分隔)</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
