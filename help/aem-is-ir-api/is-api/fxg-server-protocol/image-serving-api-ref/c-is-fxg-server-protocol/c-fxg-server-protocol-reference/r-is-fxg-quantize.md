---
description: 顏色量化。 指定GIF輸出轉換的顏色量化屬性。
solution: Experience Manager
title: 數量
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# 數量{#quantize}

顏色量化。 指定GIF輸出轉換的顏色量化屬性。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac}浮動 </span> 視窗類型 </p> <p>選擇「<span class="codeph"> web </span>」或「<span class="codeph"> mac </span>」以選擇預定義的調色板，或將設定為「<span class="codeph">自適應</span>」以計算影像的最佳調色板。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 抖動  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {dusfre|off}抖動 </span> 選項 </p> <p>為Floyd-Steinberg錯誤擴散選擇「擴散」或「關閉」以禁用抖動。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>「 <span class="codeph">自適應</span>」調色板中包含的輸出顏色數（整數）。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> 必須介於2和256之間。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>以逗號分隔的十六進位6格式強制RGB顏色清單。 允許指定要包含在「 <span class="codeph">自適應</span>」調色板中的強制顏色。 如果指定的顏色數小於<span class="codeph"> numColors </span>，則根據影像內容計算附加顏色。 </p> <p>僅當<span class="codeph"> fmt=gif </span>或<span class="codeph"> fmt=gif-alpha </span>時使用。 否則忽略。 使用<span class="codeph"> <span class="varname"> colorList </span> </span>指定的顏色必須是十六進位6格式的RGB值（請參閱<span class="codeph"> color </span>）;不允許使用其他顏色說明符。 </p> </td> 
 </tr> 
</table>

## 預設 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 範例 {#section-b3a979dc9ae3459baa093bf17310988f}

使用「 `web`」調色板生成GIF縮略圖，且不抖動：

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

將影像轉換為雙色調GIF，具有鍵色透明度，並強制將顏色轉換為黑白：

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
