---
title: setLocalizedTexts
description: Interactive Video Viewer的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2fd557ad-088a-4ddc-8c00-b3cf3d2d9a2f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

Interactive Video Viewer的JavaScript API參考。

` setLocalizedTexts( *`本地化資訊`*)`

設定一個或多個區域設定的本地化SYMBOL值。 此參數必須在 `init()`。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 本地化資訊 </span> </span> </p> </td> 
   <td colname="col2"> <p> { 0} <span class="codeph"> 對象 </span>}包含本地化資料的JSON對象。 </p> <p>請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 用戶介面元素的本地化 </a> 的子菜單。 </p> <p>另請參閱 <i>查看器SDK使用手冊</i> 以及有關對象內容的詳細資訊的示例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

另請參閱 [初始化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
