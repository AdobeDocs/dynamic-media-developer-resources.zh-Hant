---
description: 銳化紋理。 指定渲染此材料時要應用的銳利化。
solution: Experience Manager
title: 銳利
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 6%

---

# 銳利{#sharp}

銳化紋理。 指定渲染此材料時要應用的銳利化。

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>沒有銳利化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>正常銳利化（延遲）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0個替代銳利化（較早）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>更銳利化（早期和後期）。 </p> </td> 
 </tr> 
</table>

`sharp=1` 會在材料呈現後套用銳利化； `sharp=2` 在初始縮放紋理後應用銳利化，但在將其轉換為場景之前； `sharp=3` 會在轉換前後套用銳利化。

銳利化演算法和銳利化量以及其他USM（非銳利化遮色片）參數由暈映提供的預設材料模板或`rs=`控制。

## 屬性 {#section-498ec9fcb8eb415fb99532d36c11d4c7}

材料屬性。 被實色材料忽略。

## 預設 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`，除非材料是根據目錄項目，否則 `attribute::Sharp`。

## 另請參閱 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[目錄：:Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e),  [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
