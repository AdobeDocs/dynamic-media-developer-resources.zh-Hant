---
title: 量化
description: 色彩量化。 指定GIF輸出轉換的色彩量化屬性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# 量化{#quantize}

色彩量化。 指定GIF輸出轉換的色彩量化屬性。

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">型別</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>指定調色盤型別。 </p> <p>設定為<span class="codeph">最適化</span>以計算影像的最佳調色盤。 </p> <p>設定為<span class="codeph"> Web </span>或<span class="codeph"> Mac </span>以選擇預先定義的調色盤。 </p> <p> <p>注意： <span class="codeph"> mac </span>托盤型別僅支援GIF和PNG8格式，不支援GIFAlpha和PNG8Alpha格式。</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">遞色</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {擴散|關閉} </span> </p> <p>指定遞色選項。 </p> <p>針對Floyd-Steinberg誤差擴散設定為<span class="codeph">擴散</span> </p> <p>設定<span class="codeph">關閉</span>以停用遞色。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>輸出色彩的數目(2-256) </p> <p>指定<span class="codeph">最適化</span>調色盤中包含多少色彩。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">色彩清單</span> </span> </p> </td> 
   <td colname="col2"> <p>以逗號分隔的強制十六進位RGB顏色清單 </p> <p>可讓您指定要包含在<span class="codeph">最適化</span>調色盤中的色彩。 如果指定的色彩數目小於<span class="codeph"> <span class="varname"> numColors </span> </span>，則會根據影像內容計算其他色彩。</p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8ab5035055b24b858270d260912a7f3d}

要求屬性。 無論目前的圖層設定為何，都適用。 僅在`fmt=gif`、`fmt=gif-alpha`、`fmt=png8`或`fmt=png8-alpha`時使用。 否則會忽略。

以&#x200B;*`colorList`*&#x200B;指定的色彩必須包含hex6格式的RGB值（請參閱不含`0x`首碼的[色彩](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md)）。 不允許使用其他顏色規範。 修飾元&#x200B;*`numColors`*&#x200B;必須是2-256。

## 預設 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 範例 {#section-e34aca7587d548a7ae9d4266b80c9451}

使用`web`調色盤產生GIF縮圖，且無遞色：

`http:// *`*伺服器*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

將影像轉換為具有關鍵色彩透明度的雙調GIF。 而且，強制色彩為黑白：

`http:// *`*伺服器*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 另請參閱 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ， [色彩](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
