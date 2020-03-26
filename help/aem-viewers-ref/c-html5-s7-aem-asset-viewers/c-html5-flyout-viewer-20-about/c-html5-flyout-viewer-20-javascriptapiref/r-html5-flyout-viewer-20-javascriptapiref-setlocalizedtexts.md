---
description: 彈出檢視器的JavaScript API參考。
seo-description: 彈出檢視器的JavaScript API參考。
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic media
uuid: 69341735-5ebe-4e3b-acad-b6b916b11bb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setLocalizedTexts{#setlocalizedtexts}

彈出檢視器的JavaScript API參考。

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 本地化 <span class="varname"> 資訊 </span></span> </p> </td> 
   <td colname="col2"> <p> {物 <span class="codeph"> 件} </span>JSON物件與本地化資料。 </p> <p>如需詳 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> 細資訊，請參閱使用者介面元 </a> 素的本地化。 </p> <p>如需 <i></i> 物件內容的詳細資訊，請參閱Viewer SDK使用指南和範例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定一個或多個地區設定的本地化SYMBOL值。 此參數必須先呼叫 `init()`。

另請參見 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom"},"fr":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer"},defaultLocale:"en"})
```

