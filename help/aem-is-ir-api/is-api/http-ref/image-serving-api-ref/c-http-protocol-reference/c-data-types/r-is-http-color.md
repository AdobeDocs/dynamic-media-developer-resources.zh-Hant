---
description: 顏色值。 您可以使用十六進位符號、以逗號分隔的元件值清單或小數來指定顏色值。
solution: Experience Manager
title: 色彩
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 14%

---


# color{#color}

顏色值。 您可以使用十六進位符號、以逗號分隔的元件值清單或小數來指定顏色值。

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 顏色</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">{{<span class="varname"> gray</span>[,<span class="varname"> alpha</span>][g]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> red</span>,<span class="varname"> green</span>,<span class="varname"> blue</span>[,rgbAlpha<span class="varname"> </span>+[r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> {</span>agenta <span class="varname"> , magenta</span>，黃 <span class="varname"> 色，黑</span>色青色 <span class="varname"> </span>[ alpha]k}</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 紅色</span>、綠 <span class="varname"> 色</span>、藍 <span class="varname"> 色</span>、 <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>顏色元件值（0...255，小數點） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 青色</span>、洋紅色 <span class="varname"> 、黃</span>色 <span class="varname"> 、黑</span>色 <span class="varname"> 、 </span> <span class="varname"> alpha</span></span> </p></td> 
  <td class="stentry"> <p>CMYK色彩元件值（0..100 %，十進位整數） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 灰色</span>,  <span class="varname"> alpha</span></span> </p> </td> 
  <td class="stentry"> <p>灰色分量值（0...100%，小數點） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 十六進位</span> </span> </p></td> 
  <td class="stentry"> <p>封裝的兩位十六進位灰色值(GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 十六進位4</span> </span> </p> </td> 
  <td class="stentry"> <p>4位十六進位灰階，含alpha色值(GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>包含6位十六進位RGB顏色值(RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>封裝的八位十六進位RGBA(RRGGBBAA)或CMYK(CCMMYYKK)色彩值（如果以'k'字尾指定） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>帶有字母值的10位數十六進位CMYK(CCYMMKKAA) </p> </td> 
 </tr> 
</table>

RGB顏色的小數分量值在0...255範圍內。 CMYK和灰色的小數值在0.100%範圍內。 所有十六進位元件值都在0...0xFF範圍內。

顏色分量值假設與alpha值無關（未預乘）。

所有顏色值、字首和字尾都不區分大小寫。

CMYK顏色值需要字尾&#39;k&#39;。 可以為RGB和灰色值指定文字尾碼。

十六進位灰色值需要前置詞&#39;0x&#39;。

&#39;s&#39;尾碼指定顏色值與與顏色值的像素類型（定義為`attribute::IccProfileSrc*`）對應的輸入（源）顏色空間相關聯。 如果此尾碼不存在，則顏色值與輸出（目標）顏色空間（由`icc=`或`attribute::IccProfile*`定義）相關聯。

## 預設 {#section-737082a7da544acca8092a48d88480e7}

如果未明確指定alpha值，則假定為255、0xFF或100%（完全不透明）。

## 範例 {#section-4ac69026349949f8b595a6d4a9ce474d}

有效顏色指定符的一些示例及其對應的像素類型、顏色值、Alpha值和預設顏色空間：

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>顏色</i> </b> </th> 
   <th class="entry"> <b>像素類型</b> </th> 
   <th class="entry"> <b>顏色值</b> </th> 
   <th class="entry"> <b>Alpha值</b> </th> 
   <th class="entry"> <b>預設色域  </b> </th> 
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
   <td> <p>0,100,200,200rs </p> </td> 
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
   <td> <p>16017.7194萬 </p> </td> 
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
   <td> <p>0xddegs </p> </td> 
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
   <td> <p>2223242526ks </p> </td> 
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
   <td> <p>百分之十至十一至十二至十三 </p> </td> 
   <td> <p>14% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

當輸出顏色的像素類型與輸出影像的像素類型相對應時，使用`icc=`指定的輸出顏色空間會被應用，而不是預設顏色空間。
