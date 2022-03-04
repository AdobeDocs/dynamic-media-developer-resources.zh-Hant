---
title: 顏色值
description: 顏色=和bgc=屬性的顏色值可以使用十進位、逗號分隔的元件值清單或十六進位表示法指定，類似於HTML。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 608ff0f1-4fbd-4e32-af07-3a62569d14c7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 13%

---

# 顏色值{#color-values}

顏色值 `color=` 和 `bgc=` 可以使用十進位、逗號分隔的元件值清單或十六進位表示法(類似於HTML)指定屬性。

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> color</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{ {red, green, blue} |灰色} | { [ 0x hex6 } | { 0xhex2 }</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>紅，綠，藍，灰</i> </p></td> 
  <td class="stentry"> <p>顏色分量值（0...255，十進位整數）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>十六進位</i> </p></td> 
  <td class="stentry"> <p>已打包的六位十六進位RGB顏色值(RRGGBB)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>十六進位</i> </p></td> 
  <td class="stentry"> <p>已打包的兩位十六進位灰色值(0...FF)。 </p></td> 
 </tr> 
</table>

## 範例 {#section-a78732151d584e84abeb99f9ce8d7c24}

有效顏色說明符的一些示例及其相應的RGB顏色值解釋：

<table id="simpletable_837B3173020240A5B7B2DB2F4CC57352"> 
 <tr class="strow"> 
  <td class="stentry"> <p>010.02萬 </p></td> 
  <td class="stentry"> <p>(0,100,200) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>128 </p></td> 
  <td class="stentry"> <p>(128128128) </p></td> 
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

[顏色=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)。 [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0)。 [灌漿=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
