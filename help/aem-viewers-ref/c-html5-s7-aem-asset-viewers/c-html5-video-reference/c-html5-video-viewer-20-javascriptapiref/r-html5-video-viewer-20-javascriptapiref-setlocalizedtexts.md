---
title: setLocalizedTexts
description: setLocalizedTexts
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 3bb1d277-e057-4a5d-9498-2adbca8f12b2
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 5%

---

# setLocalizedTexts{#setlocalizedtexts}

` setLocalizedTexts( *`本地化資訊`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 本地化資訊 </span> </span> </p> </td> 
   <td colname="col2"> <p> { 0} <span class="codeph"> 對象 </span>}包含本地化資料的JSON對象。 </p> <p>請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> 查看器SDK命名空間 </a> 的子菜單。 </p> <p>查看 <i>查看器SDK使用手冊</i> 以及有關對象內容的詳細資訊的示例。 選填。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定一個或多個區域設定的本地化SYMBOL值。 此參數必須在 `init()`。

另請參閱 [初始化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
