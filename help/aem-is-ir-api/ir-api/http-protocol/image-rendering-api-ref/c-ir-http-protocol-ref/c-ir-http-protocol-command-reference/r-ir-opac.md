---
title: Opac
description: 不透明度. 指定材料不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# Opac{#opac}

不透明度. 指定材料不透明度。

` opac= *`谷`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 谷 </span> </p> </td> 
  <td class="stentry"> <p>材料不透明度（百分比）;0..100 </p> </td> 
 </tr> 
</table>

以下材料/對象組合支援可變不透明度：

* 應用於紋理重疊對象的實色和可重複紋理。
* 應用於窗口覆蓋框架對象的窗口覆蓋材料。
* 應用於紋理對象或壁對象的貼花。

如果材料包括帶有α通道的影像， `opac=` 可以使影像更透明，但不能使影像更不透明。

## 屬性 {#section-352f7b82ede54159b6afb90ae4b559ec}

物料屬性。 如果當前對象選取或材料不支援不透明度，則忽略。

## 預設 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`)。
