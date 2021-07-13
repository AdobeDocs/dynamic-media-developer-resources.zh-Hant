---
description: 預設材料銳利化。 設定預設材料銳利化模式，以備特定目錄記錄不包含有效的目錄銳利值時使用。
solution: Experience Manager
title: Sharp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 10%

---

# 銳利{#sharp}

預設材料銳利化。 設定預設材料銳利化模式，以備特定目錄記錄不包含有效目錄：:Sharp值時使用。

## 屬性 {#section-dcb810d01b8a40eb991d555a3cbe48b9}

列舉。

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>沒有銳利化。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>正常銳利化（在轉換後）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>替代銳利化（在轉換之前）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>更銳利化（轉換前後）。 </p> </td> 
 </tr> 
</table>

## 預設 {#section-613130fca7c04ce7a7734265f27aa1ea}

如果未定義或為空，則從`default::Sharp`繼承。

## 另請參閱 {#section-7771824f2822443ab0297e8793bb48ae}

[目錄：:Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a),  [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
