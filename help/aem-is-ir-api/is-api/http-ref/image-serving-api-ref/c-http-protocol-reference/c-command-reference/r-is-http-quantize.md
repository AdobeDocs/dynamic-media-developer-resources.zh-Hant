---
description: 色彩量化。 指定GIF輸出轉換的顏色量化屬性。
seo-description: 色彩量化。 指定GIF輸出轉換的顏色量化屬性。
seo-title: 量化
solution: Experience Manager
title: 量化
topic: Scene7 Image Serving - Image Rendering API
uuid: 4e9c4807-59bc-4eb9-bcab-0bf0cfdf56d4
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 量化{#quantize}

色彩量化。 指定GIF輸出轉換的顏色量化屬性。

` quantize= *``*[, *``*[, *``*[, *`TypedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 類型 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>指定浮動視窗類型。 </p> <p>設為可 <span class="codeph"> 自適 </span> 應計算影像的最佳浮動視窗。 </p> <p>設定為 <span class="codeph"> Web </span> 或 <span class="codeph"> Mac以 </span> 選擇預先定義的浮動視窗。 </p> <p> <p>注意： GIF <span class="codeph"> 和PNG8格 </span> 式僅支援Mac托盤類型，而GIF-Alpha和PNG8-Alpha格式則不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 混色 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {dussure|off} </span> </p> <p>指定混色選項。 </p> <p>Floyd-Steinberg誤 <span class="codeph"> 差擴 </span> 散的設定 </p> <p>設為 <span class="codeph"> 關閉 </span> 可停用混色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 數色 </span></span> </p> </td> 
   <td colname="col2"> <p>輸出顏色數(2-256) </p> <p>指定最適化浮動視窗中包含 <span class="codeph"> 多少 </span> 顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顏 <span class="varname"> 色清單 </span></span> </p> </td> 
   <td colname="col2"> <p>以逗號分隔的十六進位6格式強制RGB色彩清單 </p> <p>可讓您指定要包含在最適化色盤 <span class="codeph"> 中的 </span> 顏色。 如果指定的顏色數少於 <span class="codeph"> numColors <span class="varname"> ，則會根據影像內容 </span></span>計算其他顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8ab5035055b24b858270d260912a7f3d}

請求屬性。 不論目前的圖層設定如何，都適用。 僅用於 `fmt=gif`、 `fmt=gif-alpha`、 `fmt=png8`或時 `fmt=png8-alpha`。 否則將忽略。

使用colorList指定 ` *`的顏色`*` ，必須由十六進位6格式的RGB值組成(請參閱 ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`)，不含「 `0x`」首碼。 不允許使用其他顏色說明符。 *`numColors`* 必須介於2-256之間。

## 預設 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 範例 {#section-e34aca7587d548a7ae9d4266b80c9451}

使用浮動視窗產生GIF縮 `web` 圖，而無混色：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

將影像轉換為雙色調GIF，具有關鍵色透明度，並強制色彩轉換為黑白：

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 另請參閱 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
