---
description: 不透明度. 指定材料不透明度。
solution: Experience Manager
title: opac
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# opac{#opac}

不透明度. 指定材料不透明度。

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>材料不透明度（百分比）;0..100 </p> </td> 
 </tr> 
</table>

以下材料/對象組合支援可變不透明度：

* 實色和可重複的紋理，套用至文字重疊物件。
* 用於覆蓋框體的窗蓋材料。
* 貼上到文字對象或壁對象的標籤。

如果材料包括帶有α通道的影像，則`opac=`可用於使影像更透明，但不更不透明。

## 屬性 {#section-352f7b82ede54159b6afb90ae4b559ec}

材料屬性。 如果當前對象選擇或材料不支援不透明度，則忽略此選項。

## 預設 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`，適用於完全不透明的材料（如果影像不包含alpha通道）。
