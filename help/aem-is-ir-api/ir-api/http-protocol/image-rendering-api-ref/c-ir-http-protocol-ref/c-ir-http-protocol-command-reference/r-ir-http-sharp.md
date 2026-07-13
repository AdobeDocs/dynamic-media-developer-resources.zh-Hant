---
title: 銳利化
description: 銳利化紋理。 指定呈現此材質時要套用的銳利化。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
TQID: 'https://experienceleague.adobe.com/AWUw6E0xSWAsMfijewBvnSC8JdM5l9-qtFNLZsweFRY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 5%

---

# 銳利化{#sharp}

銳利化紋理。 指定呈現此材質時要套用的銳利化。

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>不銳利化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>一般銳利化（延遲）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0替代銳利化（早期）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>更銳利化（早和晚）。 </p> </td> 
 </tr> 
</table>

`sharp=1`在材質演算後套用銳利化；`sharp=2`在初始縮放紋理之後，但在轉換為場景之前套用銳利化；`sharp=3`在轉換之前和之後都套用銳利化。

銳利化演演算法、銳利化量和其他USM （不銳利化遮色片）引數是由暈映提供的預設材質範本或使用`rs=`所控制。

## 屬性 {#section-498ec9fcb8eb415fb99532d36c11d4c7}

材質屬性。 被純色材料忽略。

## 預設 {#section-febfa16e65864987b4d328e2ff1df64d}

如果素材是以目錄專案為基礎，`catalog::Sharp`，否則`attribute::Sharp`。

## 另請參閱 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[目錄：：銳利化](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ， [銳利化=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e)， [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)

