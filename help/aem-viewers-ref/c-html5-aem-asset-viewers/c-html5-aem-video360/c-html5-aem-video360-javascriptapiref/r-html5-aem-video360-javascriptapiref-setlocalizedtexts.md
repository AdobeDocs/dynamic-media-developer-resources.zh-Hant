---
description: Video360檢視器的JavaScript API參考。
solution: Experience Manager
title: setLocalizedTexts
feature: Dynamic Media經典，檢視器，SDK/API,360 VR視訊
role: 開發人員，商業從業人員
exl-id: b0434886-defa-47d4-9853-bfd73c64d036
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

Video360檢視器的JavaScript API參考。

` setLocalizedTexts( *`localizationInfo`*)`

設定一個或多個地區設定的本地化SYMBOL值。 必須在`init()`之前呼叫此參數。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo  </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph">物件</span>} JSON物件與本地化資料。 </p> <p>如需詳細資訊，請參閱<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local">使用者介面元素的本地化。</a> </p> <p>另請參閱<i>檢視器SDK使用指南</i>和範例，以取得有關物件內容的詳細資訊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

另請參閱[init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
