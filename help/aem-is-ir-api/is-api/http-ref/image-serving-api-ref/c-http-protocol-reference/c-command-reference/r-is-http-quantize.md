---
description: 顏色量化。 指定GIF輸出轉換的顏色量化屬性。
solution: Experience Manager
title: 數量
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 3%

---

# 數量{#quantize}

顏色量化。 指定GIF輸出轉換的顏色量化屬性。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac}  </span> </p> <p>指定浮動視窗類型。 </p> <p>設為<span class="codeph">適用性</span> ，以計算影像的最佳浮動視窗。 </p> <p>設為<span class="codeph"> web </span>或<span class="codeph"> mac </span> ，以選擇預先定義的浮動視窗。 </p> <p> <p>注意： <span class="codeph"> mac </span>托盤類型僅支援GIF和PNG8格式，而不支援GIF-Alpha和PNG8-Alpha格式。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 抖動  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {dusfre|off}  </span> </p> <p>指定抖動選項。 </p> <p>設為<span class="codeph">擴散</span>，用於Floyd-Steinberg誤差擴散 </p> <p>設為<span class="codeph"> of </span>以禁用抖動。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>輸出顏色數(2-256) </p> <p>指定<span class="codeph">自適應</span>調色板中包含的顏色數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>以逗號分隔的十六進位6格式強制RGB顏色清單 </p> <p>可讓您指定要包含在<span class="codeph">自適應</span>調色盤中的顏色。 如果指定的顏色數小於<span class="codeph"> <span class="varname"> numColors </span> </span>，則根據影像內容計算附加顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8ab5035055b24b858270d260912a7f3d}

要求屬性。 無論目前的層設定為何皆適用。 僅當`fmt=gif`、`fmt=gif-alpha`、`fmt=png8`或`fmt=png8-alpha`時使用。 否則忽略。

使用`*`colorList`*`指定的顏色必須由十六進位6格式的RGB值組成（請參閱` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`），不含「 `0x`」前置詞。 不允許使用其他顏色說明符。 *`numColors`* 必須介於2-256之間。

## 預設 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 範例 {#section-e34aca7587d548a7ae9d4266b80c9451}

使用`web`浮動視窗產生GIF縮圖，且無抖動：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

將影像轉換為雙色調GIF，具有鍵色透明度，並強制將顏色轉換為黑白：

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 另請參閱 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ，顏 [色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
