---
description: 色彩值。 您可以使用十六進位標籤法、以逗號分隔的元件值清單或小數位數來指定顏色值。
solution: Experience Manager
title: 色彩
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eba88ff0-877d-432e-bbd6-9172f5b460e9
source-git-commit: 2ff380ad30911a85bc066ae53f0cb69360ed99e4
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 3%

---

# 色彩{#color}

色彩值。 您可以使用十六進位標籤法、以逗號分隔的元件值清單或小數位數來指定顏色值。

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">色彩</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">&amp;amp；lcub；&amp;amp；lcub；<span class="varname"> gray</span>[，<span class="varname"> alpha</span>][g]&amp;amp；rcub；|</span> </p> <p> <span class="codeph"> {<span class="varname">紅色</span>，<span class="varname">綠色</span>，<span class="varname">藍色</span>[ ，<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname">青色</span>， <span class="varname">洋紅色</span>， <span class="varname">黃色</span>， <span class="varname">黑色</span>[，alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname">十六進位6</span>|<span class="varname">十六進位8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname">十六進位8</span>|<span class="varname">十六進位10</span>}k}&amp;amp；rcub；[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">紅色</span>，<span class="varname">綠色</span>，<span class="varname">藍色</span>，<span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>色彩元件值（0到255，十進位int） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">青色</span>，<span class="varname">洋紅色</span>，<span class="varname">黃色</span>，<span class="varname">黑色</span>，<span class="varname">阿爾法</span></span> </p></td> 
  <td class="stentry"> <p>CMYK色彩元件值（0..100 %，十進位int） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> gray</span>， <span class="varname"> alpha</span></span> </p> </td> 
  <td class="stentry"> <p>灰色元件值（0到100%，十進位整數） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">十六進位2</span> </span> </p></td> 
  <td class="stentry"> <p>壓縮的兩位數十六進位灰色值(GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">十六進位4</span> </span> </p> </td> 
  <td class="stentry"> <p>以Alpha色彩值壓縮四位數的十六進位灰色(GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">十六進位6</span> </span> </p> </td> 
  <td class="stentry"> <p>壓縮的六位十六進位RGB色彩值(RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">十六進位8</span> </span> </p> </td> 
  <td class="stentry"> <p>已封裝八位數的十六進位RGBA (RRGGBBAA)或CMYK (CCMMYKK)色彩值（若以'k'尾碼指定） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">十六進位10</span> </span> </p></td> 
  <td class="stentry"> <p>以Alpha值封裝10位數的十六進位CMYK (CCYYMMKKAA) </p> </td> 
 </tr> 
</table>

RGB顏色的小數元件值在0到255的範圍內。 CMYK和灰度的十進位元件值在0..100%範圍內。 所有十六進位元件值都在0到0的範圍內。

假設顏色元件值與Alpha值無關（不是預乘）。

所有色彩值、首碼和尾碼均不區分大小寫。

CMYK色彩值需要型別字尾&#39;k&#39;。 您可以選擇為RGB和灰色值指定型別字尾。

十六進位灰色的值需要前置詞&#39;0x&#39;。

&#39;s&#39;尾碼指定色彩值與對應至色彩值畫素型別（以`attribute::IccProfileSrc*`定義）的輸入（來源）色域相關聯。 如果此尾碼不存在，則色彩值與輸出（目的地）色域相關聯（以`icc=`或`attribute::IccProfile*`定義）。

## 預設 {#section-737082a7da544acca8092a48d88480e7}

如果未明確指定Alpha值，則會假設為255、0xFF或100% （完全不透明）。

## 範例 {#section-4ac69026349949f8b595a6d4a9ce474d}

有效色彩指定符號及其對應畫素型別、色彩值、Alpha值和預設色域的部分範例：

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>色彩</i> </b> </th> 
   <th class="entry"> <b>畫素型別</b> </th> 
   <th class="entry"> <b>色彩值</b> </th> 
   <th class="entry"> <b>Alpha值</b> </th> 
   <th class="entry"> <b>預設色域</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0,100,200,200rs </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203S </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>1,2，3 </p> </td> 
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
   <td> <p>100秒 </p> </td> 
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
   <td> <p> <span class="codeph"> IccProfileSrcGray </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33k </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26KS </p> </td> 
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

當輸出色彩的畫素型別對應到輸出影像的畫素型別時，會套用以`icc=`指定的輸出色域，而非預設色域。
