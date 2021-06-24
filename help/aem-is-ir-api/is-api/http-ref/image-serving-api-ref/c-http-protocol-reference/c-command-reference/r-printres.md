---
description: 打印解析度。 覆蓋嵌入在響應影像中的打印解析度值。
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# printRes{#printres}

打印解析度。 覆蓋嵌入在響應影像中的打印解析度值。

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>打印解析度(dpi)。 </p></td> 
 </tr> 
</table>

打印解析度通常由`catalog::PrintResolution`定義，如果是目錄條目，則由嵌入源影像中的打印解析度值定義。 對於模板或分層複合影像，在響應檔案中嵌入的預設打印解析度是具有最低圖層編號的圖層影像的打印解析度。

設定列印解析度不會變更回覆影像的像素大小。

## 屬性 {#section-03c7910ebe234804a319e5d0d8ef3a74}

要求屬性。 無論目前的層設定為何，都適用。

## 預設 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` 或嵌入源影像中的打印解析度。

## 另請參閱 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[目錄：:PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
