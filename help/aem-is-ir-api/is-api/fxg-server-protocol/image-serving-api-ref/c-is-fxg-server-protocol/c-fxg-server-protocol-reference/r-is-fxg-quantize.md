---
description: 顏色量化。 指定GIF輸出轉換的顏色量化屬性。
solution: Experience Manager
title: 量化
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# 量化{#quantize}

顏色量化。 指定GIF輸出轉換的顏色量化屬性。

` quantize= *`類型`*[, *`抖動`*[, *`數字顏色`*[, *`顏色清單`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 類型 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> 調色板類型 </p> <p>選擇「 <span class="codeph"> 網 </span>或 <span class="codeph"> mac </span>「 」，選擇預定義的調色板，或設定為「 <span class="codeph"> 自適應 </span>'以計算影像的最佳調色板。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 抖動 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {dusfle|off} </span> 抖動選項 </p> <p>為Floyd-Steinberg誤差擴散選擇「dusse」或「off」以禁用抖動。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 數字顏色 </span> </span> </p> </td> 
  <td class="stentry"> <p>「 」中包含的輸出顏色（整數）的數量 <span class="codeph"> 自適應 </span>'調色板。 </p> <p> <span class="codeph"> <span class="varname"> 數字顏色 </span> </span> 必須介於2和256之間。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 顏色清單 </span> </span> </p> </td> 
  <td class="stentry"> <p>以逗號分隔的十六進位6格式強制RGB顏色清單。 允許您指定要包含在「」中的強制顏色 <span class="codeph"> 自適應 </span>'調色板。 如果指定的顏色數小於 <span class="codeph"> 數字顏色 </span>，根據影像內容計算附加顏色。 </p> <p>僅在 <span class="codeph"> fmt=gif </span> 或 <span class="codeph"> fmt=gif </span>。 否則忽略。 指定的顏色 <span class="codeph"> <span class="varname"> 顏色清單 </span> </span> 必須是十六進位6格式的RGB值(請參見 <span class="codeph"> 顏色 </span>);不允許使用其他顏色說明符。 </p> </td> 
 </tr> 
</table>

## 預設 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 範例 {#section-b3a979dc9ae3459baa093bf17310988f}

使用「 」生成GIF縮略圖 `web`「調色板，無抖動：

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

將影像轉換為具有鍵色透明度的雙調GIF，並將強制顏色轉換為黑白：

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
