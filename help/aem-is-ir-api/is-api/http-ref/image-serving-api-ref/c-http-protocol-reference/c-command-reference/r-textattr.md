---
description: 文字圖層屬性。 為無法作為rtf命令使用的文本圖層指定其他屬性。
seo-description: 文字圖層屬性。 為無法作為rtf命令使用的文本圖層指定其他屬性。
seo-title: textAttr
solution: Experience Manager
title: textAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 07b3d263-2ed6-4363-83e1-3b841e9967c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# textAttr{#textattr}

文字圖層屬性。 為無法作為rtf命令使用的文本圖層指定其他屬性。

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span></span> </p> </td> 
  <td class="stentry"> <p>提供縮放文字圖層而不變更字型大小的方式。 較高解析度的值會增加轉譯文字相對於畫布大小的大小；值越小，文字大小就越小。 文字解析度（單位為每英吋點數）（整數大於0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 消 <span class="varname"> 除鋸齒 </span></span> </p> </td> 
  <td class="stentry"> <p>控制文字轉換引擎採用的抗鋸齒模式。 </p> <p> <span class="codeph"> off|基準|清晰|銳利| strong|平滑 </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 關閉 </span> </p> </td> 
      <td class="stentry"> <p>停用文字消除鋸齒。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 規範 </span> </p> </td> 
      <td class="stentry"> <p>啟用標準文字消除鋸齒模式（預設）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 清脆 </span> </p> </td> 
      <td class="stentry"> <p>選擇Photoshop消除鋸齒模式 <span class="codeph"> 清晰 </span> (僅 <span class="codeph"> 限文本 </span> Ps=)。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 銳利 </span> </p> </td> 
      <td class="stentry"> <p>選取Photoshop消除鋸齒模式 <span class="codeph"> 銳利 </span> (僅 <span class="codeph"> 限文 </span> 字Ps=)。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 強 </span> </p> </td> 
      <td class="stentry"> <p>選擇Photoshop抗鋸齒模式 <span class="codeph"> 強 </span> 化( <span class="codeph"> 僅限 </span> 文字Ps=)。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>控制轉換文字時使用解析度的方式 </p> <p> <span class="codeph"> fixedRes| autoRes| maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>使用指定的解析度。 </p> <p>如果要以與合成畫布完全相同的大小呈現文字，請使用。 如果文字方塊太小，文字可能會被裁切為圖層大小（如果已指定）。 這是文字 <span class="varname"> Ps= </span> 唯一支援的 <span class="codeph"> resMode選項 </span>。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>自動調整解析度，以最佳方式將圖層填滿文字。 </p> <p>使用可自動調整文字大小，讓文字方塊盡可能填滿，而不會有截斷的風險。 如果啟用換行，文字可能會以最終解析度重新換行。 <span class="varname"> 如果 </span> 選取了自動 <span class="codeph"> 重 </span> 新解析度， 文字 <span class="codeph"> Ps=不支援 </span>。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>使用指定的解析度；如果有必要，請加以減少，以防止文字截斷至圖層正確。 </p> <p>只要不發生剪裁，即可使用精確指定的解析度來轉換文字。 在剪裁的情況下，會自動降低解析度，以確保所有文字都完全包含在文字方塊中。 如果啟用換行，文字可能會以最終解析度重新換行。 文字 <span class="codeph"> Ps=不支援 </span>。 </p> </td> 
     </tr> 
    </table> </p> <p>如果未以size=指定文本圖層大小，或僅指定了寬度，則會忽略'autoRes'和'maxRes'設定，並使用指定的解析度來渲染文本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 換行 </span></span> </p> </td> 
  <td class="stentry"> <p>指定包裝模式。 </p> <p> <span class="codeph"> 繞圈|無包裝| nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>停用換行。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 換行 </span> </p> </td> 
      <td class="stentry"> <p>啟用標準換行。 </p> <p>視需要將長字切換。 <span class="codeph"> textPs=僅 </span> 支援換 <span class="codeph"> 行 </span>。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>啟用不中斷的換行。 </p> <p>一個字詞永遠不會斷，即使結尾被截斷。 通常與autoRes或maxRes <span class="codeph"> 搭配使 </span> 用， <span class="codeph"> 以確 </span> 保長字詞不會中斷。 </p> </td> 
     </tr> 
    </table> </p> <p>在文 <span class="codeph"> 字邊 </span> 界和連 <span class="codeph"> 字型大小 </span> 上自動換行和換行。 </p> </td> 
 </tr> 
</table>

## 屬性 {#section-114ca0b8585b403c873e2251478ad1d5}

文字圖層屬性。 被影像、純色和效果圖層忽略。 如果已 `layer=0` 指定，則套用至 `layer=comp`。

## 預設 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 另請參閱 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
