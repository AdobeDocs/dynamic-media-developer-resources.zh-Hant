---
description: 可以使用十進位、逗號分隔的元件值清單或十六進位表示法（類似於HTML）來指定color=和bgc=屬性的顏色值。
solution: Experience Manager
title: 顏色值
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 11%

---


# 顏色值{#color-values}

可以使用十進位、逗號分隔的元件值清單或十六進位表示法（類似於HTML）來指定color=和bgc=屬性的顏色值。

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> color</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{ {red, green, blue} |灰色} | { [ 0x ] hex6 } | { 0xhex2 }</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>紅，綠，藍，灰色</i> </p></td> 
  <td class="stentry"> <p>顏色元件值（0...255，小數整數）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex6</i> </p></td> 
  <td class="stentry"> <p>包含6位數的十六進位RGB顏色值(RRGGBB)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>十六進位</i> </p></td> 
  <td class="stentry"> <p>已打包兩位十六進位灰色值(0...FF)。 </p></td> 
 </tr> 
</table>

## 範例 {#section-a78732151d584e84abeb99f9ce8d7c24}

有效顏色指定符的一些示例及其相應的RGB顏色值解釋：

<table id="simpletable_837B3173020240A5B7B2DB2F4CC57352"> 
 <tr class="strow"> 
  <td class="stentry"> <p>010.02萬 </p></td> 
  <td class="stentry"> <p>(0,100,200) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>128 </p></td> 
  <td class="stentry"> <p>（12812.8128萬） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0x010203 </p></td> 
  <td class="stentry"> <p>(1,2,3) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>00b1c2 </p></td> 
  <td class="stentry"> <p>（16017.7194萬） </p></td> 
 </tr> 
</table>

## 另請參閱 {#section-207d5cb918a94736a27445faa58917d3}

[color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa),  [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0), [gruet=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
