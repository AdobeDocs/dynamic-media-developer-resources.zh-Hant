---
title: 鋒利
description: 銳化紋理。 指定呈現此材料時要應用的銳化。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 6%

---

# 鋒利{#sharp}

銳化紋理。 指定呈現此材料時要應用的銳化。

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>沒有磨刀。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>正常銳化（延遲）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0個備用銳化（早）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>更銳化（早和晚）。 </p> </td> 
 </tr> 
</table>

`sharp=1` 在渲染材料後應用銳化； `sharp=2` 在紋理初始縮放後，在將其轉換為場景之前，應用銳化； `sharp=3` 應用銳化變換前後。

銳化算法和銳化量以及其它USM（非銳化掩蔽）參數由視頻提供或與 `rs=`。

## 屬性 {#section-498ec9fcb8eb415fb99532d36c11d4c7}

物料屬性。 被純色材料忽略。

## 預設 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`，否則 `attribute::Sharp`。

## 另請參閱 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[目錄：：銳](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) 。 [銳化=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e)。 [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
