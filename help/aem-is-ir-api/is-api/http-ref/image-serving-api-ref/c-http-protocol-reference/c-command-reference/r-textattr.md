---
description: 文字層屬性。 為不能作為rtf命令的文本層指定其他屬性。
solution: Experience Manager
title: textAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

---

# textAttr{#textattr}

文字層屬性。 為不能作為rtf命令的文本層指定其他屬性。

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>提供了一種不更改字型大小而縮放文本圖層的方法。 較高的解析度值會增加相對於畫布大小的呈現文本的大小；值越小，文字大小就越小。 文本解析度(單位為點/英吋（整數大於0）)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing  </span> </span> </p> </td> 
  <td class="stentry"> <p>控制文本渲染引擎採用的消除鋸齒模式。 </p> <p> <span class="codeph"> 關閉 |規範 |清晰 |銳利 | strong |平滑  </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 關閉 </span> </p> </td> 
      <td class="stentry"> <p>禁用文本消除鋸齒。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 規範  </span> </p> </td> 
      <td class="stentry"> <p>啟用標準文本消除鋸齒模式（預設）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 清脆  </span> </p> </td> 
      <td class="stentry"> <p>選擇Photoshop消除鋸齒模式<span class="codeph">清晰</span>（僅<span class="codeph"> textPs= </span>）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 銳利  </span> </p> </td> 
      <td class="stentry"> <p>選擇Photoshop消除鋸齒模式<span class="codeph">銳利</span>（僅<span class="codeph"> textPs= </span>）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 強 </span> </p> </td> 
      <td class="stentry"> <p>選擇Photoshop消除鋸齒模式<span class="codeph"> strong </span>（僅限<span class="codeph"> textPs= </span>）。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>控制渲染文本時如何使用重新顯示 </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>使用指定的解析度。 </p> <p>如果要以與複合畫布完全相同的大小呈現文本，請使用。 如果文本框太小，文本可以被剪切到圖層大小（如果指定）。 這是<span class="codeph"> textPs= </span>支援的唯一<span class="varname"> resMode </span>選項。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>自動調整解析度，以最佳方式用文本填充圖層。 </p> <p>使用自動調整文本大小，使文本框盡可能地填充，而不存在截斷的風險。 如果啟用了換行，則文本可能會在最終解析度重新換行。 <span class="varname"> 如果 </span> 選取了autoRes, <span class="codeph"> 則 </span> 會忽略res。<span class="codeph"> textPs= </span>不支援。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>使用指定的解析度；如果需要，請減少，以防止文本被截斷到層直。 </p> <p>只要不發生剪切，則使用以精確指定的解析度呈現文本。 在剪裁的情況下，會自動降低解析度，以確保所有文本都完全包含在文本框內。 如果啟用了換行，則文本可能會在最終解析度重新換行。 <span class="codeph"> textPs= </span>不支援。 </p> </td> 
     </tr> 
    </table> </p> <p>如果未指定size=的文本層大小，或者只指定了寬度，則會忽略「autoRes」和「maxRes」設定，並使用指定的解析度來呈現文本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定包裝模式。 </p> <p> <span class="codeph"> 繞排 | noWrap | nbWrap  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>禁用換行。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 換行 </span> </p> </td> 
      <td class="stentry"> <p>啟用標準換行。 </p> <p>如有必要，請用長詞。 <span class="codeph"> textPs=僅 </span> 支援 <span class="codeph"> 繞排 </span>。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>啟用不斷字換行。 </p> <p>一個詞永遠不會斷，即使詞尾被截斷。 通常與<span class="codeph"> autoRes </span>或<span class="codeph"> maxRes </span>搭配使用，以確保長字詞永不中斷。 </p> </td> 
     </tr> 
    </table> </p> <p><span class="codeph">繞排</span>和<span class="codeph">繞排</span>會自動繞排字詞邊界和連字型大小。 </p> </td> 
 </tr> 
</table>

## 屬性 {#section-114ca0b8585b403c873e2251478ad1d5}

文字層屬性。 被影像、實色和效果層忽略。 如果為`layer=comp`指定，則應用於`layer=0`。

## 預設 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 另請參閱 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
