---
title: Sharp
description: 預設材料銳化。 如果特定目錄記錄不包含有效的目錄銳值，則設定預設的材料銳化模式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 11%

---

# 尖{#sharp}

預設材料銳化。 在特定目錄記錄不包含有效的目錄記錄時設定預設材料銳化模式 `catalog::Sharp` 值。

## 屬性 {#section-dcb810d01b8a40eb991d555a3cbe48b9}

枚舉。

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>沒有磨刀。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>正常銳化（轉換後）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>替代銳化（在轉換前）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>更多銳化（變換前後）。 </p> </td> 
 </tr> 
</table>

## 預設 {#section-613130fca7c04ce7a7734265f27aa1ea}

繼承自 `default::Sharp` 或為空。

## 另請參閱 {#section-7771824f2822443ab0297e8793bb48ae}

[目錄：：銳](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) 。 [急=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)。 [目錄：:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
