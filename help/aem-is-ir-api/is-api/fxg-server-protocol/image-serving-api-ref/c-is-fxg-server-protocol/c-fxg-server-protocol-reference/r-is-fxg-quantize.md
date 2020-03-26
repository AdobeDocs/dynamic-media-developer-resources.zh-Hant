---
description: 色彩量化。 指定GIF輸出轉換的顏色量化屬性。
seo-description: 色彩量化。 指定GIF輸出轉換的顏色量化屬性。
seo-title: 量化
solution: Experience Manager
title: 量化
topic: Scene7 Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 量化{#quantize}

色彩量化。 指定GIF輸出轉換的顏色量化屬性。

` quantize= *``*[, *``*[, *``*[, *`TypedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 類型 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac}浮動視窗類 </span> 型 </p> <p>選取「 <span class="codeph"> web </span>」或「 <span class="codeph"> mac」以選擇預先定義的浮動視窗，或設為「最適化」以 </span><span class="codeph"></span>計算影像的最佳浮動視窗。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 混色 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {dusmale|off}混色選 </span> 項 </p> <p>為Floyd-Steinberg錯誤擴散選取「擴散」，或選取「關閉」以停用混色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 數色 </span></span> </p> </td> 
  <td class="stentry"> <p>「最適化」浮動視窗中包含的輸出色彩( <span class="codeph"> 整 </span>數)數。 </p> <p> <span class="codeph"> 數 <span class="varname"> 字顏 </span></span> 色必須介於2和256之間。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 顏 <span class="varname"> 色清單 </span></span> </p> </td> 
  <td class="stentry"> <p>以逗號分隔的十六進位6格式強制RGB色彩清單。 可讓您指定要包含在「最適化」浮動視窗中 <span class="codeph"> 的強 </span>制色彩。 如果指定的顏色數小於 <span class="codeph"> numColors </span>，則會根據影像內容計算其他顏色。 </p> <p>僅在fmt=gif <span class="codeph"> 或 </span> fmt=gif-alpha時使用 <span class="codeph"></span>。 否則將忽略。 使用colorList指定 <span class="codeph"> 的 <span class="varname"> 顏色 </span> 必須是十六進位6格 </span> 式的RGB值(請參閱 <span class="codeph"> 顏色 </span>);不允許使用其他顏色說明符。 </p> </td> 
 </tr> 
</table>

## 預設 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 範例 {#section-b3a979dc9ae3459baa093bf17310988f}

使用「 `web`」浮動視窗產生GIF縮圖，不會混色：

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

將影像轉換為雙色調GIF，具有關鍵色透明度，並強制色彩轉換為黑白：

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
