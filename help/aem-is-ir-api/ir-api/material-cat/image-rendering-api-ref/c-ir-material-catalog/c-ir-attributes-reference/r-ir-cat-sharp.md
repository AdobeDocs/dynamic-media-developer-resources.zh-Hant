---
description: 預設材質銳利化。 設定預設材料銳利化模式，以防特定目錄記錄不包含有效的目錄銳利化值。
solution: Experience Manager
title: Sharp
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 10%

---


# Sharp{#sharp}

預設材質銳利化。 設定預設材料銳利化模式，以防特定目錄記錄不包含有效目錄：:Sharp值。

## 屬性 {#section-dcb810d01b8a40eb991d555a3cbe48b9}

列舉。

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
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
  <td class="stentry"> <p>更銳利化（變形前後都有）。 </p> </td> 
 </tr> 
</table>

## 預設 {#section-613130fca7c04ce7a7734265f27aa1ea}

如果未定義或為空，則繼承自`default::Sharp`。

## 另請參閱 {#section-7771824f2822443ab0297e8793bb48ae}

[catalog:::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a) [, catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
