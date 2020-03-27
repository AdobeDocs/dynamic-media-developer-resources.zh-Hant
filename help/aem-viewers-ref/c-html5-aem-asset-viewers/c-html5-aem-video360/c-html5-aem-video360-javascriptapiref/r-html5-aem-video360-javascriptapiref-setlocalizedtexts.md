---
description: Video360檢視器的JavaScript API參考。
seo-description: Video360檢視器的JavaScript API參考。
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic media
uuid: dd9cf899-8855-463b-a142-698fd1a650fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setLocalizedTexts{#setlocalizedtexts}

Video360檢視器的JavaScript API參考。

` setLocalizedTexts( *`localizationInfo`*)`

設定一個或多個地區設定的本地化SYMBOL值。 此參數必須先呼叫 `init()`。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 本地化 <span class="varname"> 資訊 </span></span> </p> </td> 
   <td colname="col2"> <p> {物 <span class="codeph"> 件} </span>JSON物件與本地化資料。 </p> <p>如需詳 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> 細資訊，請參閱使用者介面元 </a> 素的本地化。 </p> <p>另請參閱檢 <i>視器SDK使用指南</i> ，以及範例，以取得物件內容的詳細資訊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

另請參見 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```

