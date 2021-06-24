---
description: 視訊檢視器的JavaScript API參考。
solution: Experience Manager
title: setLocalizedTexts
feature: Dynamic Media Classic，檢視器，SDK/API,eCatalog搜尋
role: Developer,Business Practitioner
exl-id: dfd57bde-70cd-483f-bcd4-680186e4a733
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

視訊檢視器的JavaScript API參考。

[!DNL ` setLocalizedTexts( *`localizationInfo`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> 具有本地化資料的{<span class="codeph">對象</span>} JSON對象。 </p> <p>如需詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">使用者介面元素本地化</a> 。 </p> <p>如需物件內容的詳細資訊，另請參閱<i>檢視器SDK使用指南</i>和範例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定一個或多個區域設定的本地化SYMBOL值。 必須在[!DNL `init()`]之前呼叫此參數。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
