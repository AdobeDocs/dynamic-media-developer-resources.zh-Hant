---
description: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
feature: Dynamic Media Classic，檢視器， SDK/API，影片
role: Developer,Business Practitioner
exl-id: 3bb1d277-e057-4a5d-9498-2adbca8f12b2
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# setLocalizedTexts{#setlocalizedtexts}

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo  </span> </span> </p> </td> 
   <td colname="col2"> <p> 具有本地化資料的{ <span class="codeph">對象</span>} JSON對象。 </p> <p>如需詳細資訊，請參閱<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local">檢視器SDK命名空間</a> 。 </p> <p>如需物件內容的詳細資訊，請參閱<i>檢視器SDK使用指南</i>和範例。 選填。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定一個或多個區域設定的本地化SYMBOL值。 必須在`init()`之前呼叫此參數。

另請參閱[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
