---
title: 量化
description: 顏色量化。 指定GIF輸出轉換的顏色量化屬性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 3%

---

# 量化{#quantize}

顏色量化。 指定GIF輸出轉換的顏色量化屬性。

` quantize= *`類型`*[, *`抖動`*[, *`數字顏色`*[, *`顏色清單`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 類型 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>指定調色板類型。 </p> <p>設定為 <span class="codeph"> 自適應 </span> 計算影像的最佳調色板。 </p> <p>設定為 <span class="codeph"> 網 </span> 或 <span class="codeph"> mac </span> 頁籤 </p> <p> <p>注：的 <span class="codeph"> mac </span> 托盤類型僅支援GIF和PNG8格式，但不支援GIF-Alpha和PNG8-Alpha格式。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 抖動 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {dusfle|off} </span> </p> <p>指定抖動選項。 </p> <p>設定為 <span class="codeph"> 擴散 </span> Floyd-Steinberg誤差擴散 </p> <p>設定為 <span class="codeph"> 關 </span> 禁用抖動。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 數字顏色 </span> </span> </p> </td> 
   <td colname="col2"> <p>輸出顏色數(2-256) </p> <p>指定在 <span class="codeph"> 自適應 </span> 調色板。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 顏色清單 </span> </span> </p> </td> 
   <td colname="col2"> <p>以逗號分隔的十六進位6格式強制RGB顏色清單 </p> <p>用於指定要包含在 <span class="codeph"> 自適應 </span> 調色板。 如果指定的顏色數小於 <span class="codeph"> <span class="varname"> 數字顏色 </span> </span>，根據影像內容計算附加顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8ab5035055b24b858270d260912a7f3d}

請求屬性。 應用，與當前圖層設定無關。 僅在 `fmt=gif`。 `fmt=gif-alpha`。 `fmt=png8`或 `fmt=png8-alpha`。 否則忽略。

指定的顏色 *`colorList`* 必須包含十六進位格式的RGB值(請參見 [顏色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) 無 `0x` 前置詞。 不允許使用其他顏色說明符。 *`numColors`* 必須在2-256之間。

## 預設 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 範例 {#section-e34aca7587d548a7ae9d4266b80c9451}

使用 `web` 調色板和無抖動：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

將影像轉換為具有鍵色透明度的雙調GIF，並將強制顏色轉換為黑白：

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 另請參閱 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) 。 [顏色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
