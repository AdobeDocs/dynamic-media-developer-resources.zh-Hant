---
description: 顏色值。 您可以使用十六進位記號、以逗號分隔的元件值清單或小數來指定顏色值。
solution: Experience Manager
title: 色彩
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: eba88ff0-877d-432e-bbd6-9172f5b460e9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 14%

---

# 色彩{#color}

顏色值。 您可以使用十六進位記號、以逗號分隔的元件值清單或小數來指定顏色值。

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 色彩</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">{{<span class="varname"> gray</span>[,<span class="varname"> alpha</span>][g]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> red</span>,<span class="varname"> green</span>,<span class="varname"> blue</span>[,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> 青色</span>、 <span class="varname"> 洋紅色</span>、 <span class="varname"> 黃色</span>、 <span class="varname"> 黑色</span>[,alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span> | <span class="varname"> hex10</span>}k}}[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 紅色</span>、 <span class="varname"> 綠色</span>、 <span class="varname"> 藍色</span>、 <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>顏色元件值（0...255，小數點整） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 青色</span>、 <span class="varname"> 洋紅色</span>、 <span class="varname"> 黃色</span>、 <span class="varname"> 黑色</span>、 <span class="varname"> α</span></span> </p></td> 
  <td class="stentry"> <p>CMYK顏色元件值（0.100 %，小數點） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 灰色</span>,  <span class="varname"> alpha</span></span> </p> </td> 
  <td class="stentry"> <p>灰色分量值（0...100%，小數點） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>壓縮的二位數十六進位灰色值(GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 十六進位</span> </span> </p> </td> 
  <td class="stentry"> <p>包含4位十六進位灰色，帶有alpha色值(GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>包六位數的十六進位RGB顏色值(RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>包8位數的十六進位RGBA(RRGGBBAA)或CMYK(CCMMYYKK)顏色值（如果以「k」尾碼指定） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>帶Alpha值的十進位十六進位CMYK(CCYYMMKKAA) </p> </td> 
 </tr> 
</table>

RGB顏色的十進位元件值在0...255範圍內。 CMYK和灰色的小數值在0.100%範圍內。 所有十六進位元件值都在0...0xFF範圍內。

顏色分量值被假定為與Alpha值無關（未預乘）。

所有顏色值、前置詞和尾碼均不區分大小寫。

CMYK顏色值需要類型尾碼&#39;k&#39;。 可選擇為RGB和灰色值指定類型尾碼。

十六進位灰色值需要前置詞&#39;0x&#39;。

「s」尾碼指定顏色值與與顏色值的像素類型（定義為`attribute::IccProfileSrc*`）對應的輸入（源）顏色空間相關聯。 如果此尾碼不存在，則顏色值與輸出（目標）顏色空間相關聯（由`icc=`或`attribute::IccProfile*`定義）。

## 預設 {#section-737082a7da544acca8092a48d88480e7}

如果未明確指定Alpha值，則假定它為255、0xFF或100%（完全不透明）。

## 範例 {#section-4ac69026349949f8b595a6d4a9ce474d}

有效顏色說明符的一些示例，及其對應的像素類型、顏色值、字母值和預設顏色空間：

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>色彩</i> </b> </th> 
   <th class="entry"> <b>像素類型</b> </th> 
   <th class="entry"> <b>色彩值</b> </th> 
   <th class="entry"> <b>Alpha值</b> </th> 
   <th class="entry"> <b>預設顏色空間  </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>010.02萬 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>010.02萬 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>010020.02萬rs </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>010.02萬 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203S </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>160,177,194 </p> </td> 
   <td> <p>211 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100S </p> </td> 
   <td> <p>灰色 </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75克 </p> </td> 
   <td> <p>灰色 </p> </td> 
   <td> <p>50% </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>灰色 </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeeg </p> </td> 
   <td> <p>灰色 </p> </td> 
   <td> <p>87% </p> </td> 
   <td> <p>93% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33k </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>2223242.526萬堪薩斯 </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22-23-24-25% </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56-57-58-59% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

當輸出顏色的像素類型與輸出影像的像素類型相對應時，使用`icc=`指定的輸出顏色空間應用而不是預設顏色空間。
