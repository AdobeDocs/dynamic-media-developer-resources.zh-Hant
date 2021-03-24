---
description: 銳利化. 銳利化屬性，可決定在演算期間銳利化材質的時間。
solution: Experience Manager
title: Sharp
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 10%

---


# Sharp{#sharp}

銳利化. 銳利化屬性，可決定在演算期間銳利化材質的時間。

銳利化的類型和數量由暈映透過預設材質範本或使用`catalog::RenderSettings`控制。

## 屬性 {#section-aac81b1a611b4bca90b8544eae7896df}

列舉。

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>沒有銳利化。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>正常銳利化（在變形後）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>替代銳利化（在變形前）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>更銳利化（變形前後都有）。 </p></td> 
 </tr> 
</table>

被純色材料忽略，對於所有其他材料則可選。

## 預設 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` 如果欄位不存在、空白或值不是支援的選項，則會使用此欄位。

## 另請參閱 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[屬性：：銳利化](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [目錄：:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
