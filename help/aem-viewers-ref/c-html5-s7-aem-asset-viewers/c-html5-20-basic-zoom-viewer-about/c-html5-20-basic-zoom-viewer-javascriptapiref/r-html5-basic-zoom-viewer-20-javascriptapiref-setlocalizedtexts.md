---
description: 基本縮放檢視器的JavaScript API參考。
seo-description: 基本縮放檢視器的JavaScript API參考。
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
uuid: 34a2ea4e-5493-41fa-92bf-5cebe66f6370
feature: Dynamic Media經典，檢視器，SDK/API，縮放
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---


# setLocalizedTexts{#setlocalizedtexts}

基本縮放檢視器的JavaScript API參考。

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph">物件</span>} JSON物件與本地化資料。 </p> <p>如需詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">使用者介面元素的本地化</a>。 </p> <p> 另請參閱<i>檢視器SDK使用指南</i>和範例，以取得有關物件內容的詳細資訊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定一個或多個地區設定的本地化SYMBOL值。 必須在`init()`之前呼叫此參數。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 傳回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

