---
description: 視訊檢視器的JavaScript API參考。
solution: Experience Manager
title: setLocalizedTexts
feature: Dynamic Media Classic，檢視器，SDK/API，縮放
role: Developer,User
exl-id: 8b471abe-df80-4601-bdcc-b7928418f351
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

視訊檢視器的JavaScript API參考。

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> 具有本地化資料的{<span class="codeph">對象</span>} JSON對象。 </p> <p>如需詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">使用者介面元素本地化</a> 。 </p> <p>如需物件內容的詳細資訊，請參閱<i>檢視器SDK使用手冊</i>及範例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定一個或多個區域設定的本地化SYMBOL值。 必須在`init()`之前呼叫此參數。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
