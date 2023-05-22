---
description: 文本層屬性。 指定文本圖層的附加屬性，這些屬性不可用作rtf命令。
solution: Experience Manager
title: 文本屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 1%

---

# 文本屬性{#textattr}

文本層屬性。 指定文本圖層的附加屬性，這些屬性不可用作rtf命令。

` textAttr= *`雷`*[, *`消除鋸齒`*[, *`resMode`*[, *`換行`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 雷 </span> </span> </p> </td> 
  <td class="stentry"> <p>提供一種在不更改字型大小的情況下縮放文本圖層的方法。 解析度值越高，渲染文本的大小越大；較小的值會減小文本大小。 文本解析度（以點/英吋為單位）（int大於0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 消除鋸齒 </span> </span> </p> </td> 
  <td class="stentry"> <p>控制文本渲染引擎採用的消除鋸齒模式。 </p> <p> <span class="codeph"> 關 |規範 |清晰 |銳 | strong |平滑 </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 關閉 </span> </p> </td> 
      <td class="stentry"> <p>禁用文本消除鋸齒。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 范數 </span> </p> </td> 
      <td class="stentry"> <p>啟用標準文本消除鋸齒模式（預設）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 脆 </span> </p> </td> 
      <td class="stentry"> <p>選擇Photoshop消除鋸齒模式 <span class="codeph"> 脆 </span> ( <span class="codeph"> textPs= </span> 僅)。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 鋒利 </span> </p> </td> 
      <td class="stentry"> <p>選擇Photoshop消除鋸齒模式 <span class="codeph"> 鋒利 </span> ( <span class="codeph"> textPs= </span> 僅)。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 強 </span> </p> </td> 
      <td class="stentry"> <p>選擇Photoshop消除鋸齒模式 <span class="codeph"> 強 </span> ( <span class="codeph"> textPs= </span> 僅)。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>控制渲染文本時如何使用資源 </p> <p> <span class="codeph"> 固定資源 |自動恢復 |最大資源 </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 固定資源 </span> </p> </td> 
      <td class="stentry"> <p>使用指定的解析度。 </p> <p>如果要以與合成畫布相對的精確大小呈現文本，則使用。 如果文本框太小，則文本可剪切到圖層大小（如果指定）。 這是唯一 <span class="varname"> resMode </span> 支援的選項 <span class="codeph"> textPs= </span>。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 自動恢復 </span> </p> </td> 
      <td class="stentry"> <p>自動調整解析度，以最好地用文本填充圖層。 </p> <p>用於自動調整文本大小，以便盡可能填充文本框，而不存在截斷風險。 如果啟用了換行，則文本可以在最終解析度下重新換行。 <span class="varname"> 雷 </span> 如果忽略 <span class="codeph"> 自動恢復 </span> 的子菜單。 不支援 <span class="codeph"> textPs= </span>。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 最大資源 </span> </p> </td> 
      <td class="stentry"> <p>使用指定的解析度；如果需要，請減少文本被截斷到層矩形。 </p> <p>只要不發生剪貼，則使用以精確指定的解析度呈現文本。 在剪貼時，解析度會自動降低，以確保所有文本都完全包含在文本框中。 如果啟用了換行，則文本可以在最終解析度下重新換行。 不支援 <span class="codeph"> textPs= </span>。 </p> </td> 
     </tr> 
    </table> </p> <p>如果未指定size=的文本圖層大小，或僅指定了寬度，則會忽略「autoRes」和「maxRes」設定，並使用指定的解析度來呈現文本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 換行 </span> </span> </p> </td> 
  <td class="stentry"> <p>指定包裝模式。 </p> <p> <span class="codeph"> 包 |不包裝 |nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 無包裝 </span> </p> </td> 
      <td class="stentry"> <p>禁用換行。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 換行 </span> </p> </td> 
      <td class="stentry"> <p>啟用標準換行。 </p> <p>如有必要，可以斷開長詞。 <span class="codeph"> textPs= </span> 僅支援 <span class="codeph"> 包 </span>。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>啟用非斷字換行。 </p> <p>一個詞永遠不會斷，即使它在結尾被截斷。 通常與 <span class="codeph"> 自動恢復 </span> 或 <span class="codeph"> 最大資源 </span> 確保長話不被打破。 </p> </td> 
     </tr> 
    </table> </p> <p>兩者 <span class="codeph"> 包 </span> 和 <span class="codeph"> 包 </span> 自動換行字邊界和連字元。 </p> </td> 
 </tr> 
</table>

## 屬性 {#section-114ca0b8585b403c873e2251478ad1d5}

文本層屬性。 被影像、實色和效果圖層忽略。 應用於 `layer=0` 如果指定 `layer=comp`。

## 預設 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 另請參閱 {#section-68b0d2e2d0474e2097a9331ae272c224}

[文本=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) 。 [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)。 [大小=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
