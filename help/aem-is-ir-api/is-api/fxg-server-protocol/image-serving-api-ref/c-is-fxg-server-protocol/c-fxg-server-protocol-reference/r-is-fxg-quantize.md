---
title: 量化
description: 色彩量化。 指定GIF輸出轉換的色彩量化屬性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
TQID: 'https://experienceleague.adobe.com/m5e14tLMY1JAdZTzlw7iUZzXzL9yylP66MYi5XAeYtg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# 量化{#quantize}

色彩量化。 指定GIF輸出轉換的色彩量化屬性。

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">型別</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span>調色盤型別 </p> <p>選取'<span class="codeph"> Web </span>'或'<span class="codeph"> mac </span>'以選擇預先定義的調色盤，或設定為'<span class="codeph">最適化</span>'以計算影像的最佳調色盤。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">遞色</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {擴散|關閉} </span>個遞色選項 </p> <p>選取Floyd-Steinberg誤差擴散的「擴散」或「關閉」以停用遞色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>'<span class="codeph">最適化</span>'調色盤中包含的輸出色彩數目（整數）。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span>必須介於2到256之間。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">色彩清單</span> </span> </p> </td> 
  <td class="stentry"> <p>以逗號分隔的強制十六進位RGB顏色清單。 可讓您指定要包含在'<span class="codeph">最適化</span>'調色盤中的強制色彩。 如果指定的色彩數目小於<span class="codeph"> numColors </span>，則會根據影像內容計算其他色彩。 </p> <p>僅在<span class="codeph"> fmt=gif </span>或<span class="codeph"> fmt=gif-alpha </span>時使用。 否則會忽略。 以<span class="codeph"> <span class="varname"> colorList </span> </span>指定的色彩必須是十六進位6格式的RGB值（請參閱<span class="codeph">色彩</span>）；不允許使用其他色彩指定元。 </p> </td> 
 </tr> 
</table>

## 預設 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 範例 {#section-b3a979dc9ae3459baa093bf17310988f}

使用&#39; `web`&#39;調色盤產生GIF縮圖，且無遞色：

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

將影像轉換為雙調GIF，具有關鍵色彩透明度，並強制將色彩轉換為黑白：

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
