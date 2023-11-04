---
description: 銳利化. 銳利化屬性，決定彩現時材料銳利化的時間。
solution: Experience Manager
title: Sharp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 9%

---

# Sharp{#sharp}

銳利化. 銳利化屬性，決定彩現時材料銳利化的時間。

銳利化的型別和數量是由暈映透過預設材料範本或透過控制 `catalog::RenderSettings`.

## 屬性 {#section-aac81b1a611b4bca90b8544eae7896df}

列舉。

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>不銳利化。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>一般銳利化（變形後）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>替代銳利化（變形前）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>更銳利化（變形前和變形後）。 </p></td> 
 </tr> 
</table>

被純色材料忽略，對於所有其他材料而言，這是選擇性的。

## 預設 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` 如果欄位不存在、如果欄位空白或值不是支援的選擇之一，則會使用。

## 另請參閱 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[屬性：：銳利化](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) ， [catalog：：RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd)， [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
