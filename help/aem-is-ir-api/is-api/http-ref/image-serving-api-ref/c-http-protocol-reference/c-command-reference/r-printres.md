---
description: 列印解析度。 覆寫回應影像中內嵌的列印解析度值。
seo-description: 列印解析度。 覆寫回應影像中內嵌的列印解析度值。
seo-title: printRes
solution: Experience Manager
title: printRes
uuid: 1a62611a-b3b9-4f20-834f-e34e75d33ddd
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# printRes{#printres}

列印解析度。 覆寫回應影像中內嵌的列印解析度值。

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>列印解析度(dpi)。 </p></td> 
 </tr> 
</table>

打印解析度通常由`catalog::PrintResolution`定義，如果是目錄條目，則由定義，否則由嵌入在源影像中的打印解析度值定義。 對於模板或分層複合影像，在響應檔案中嵌入的預設打印解析度是具有最低圖層編號的圖層影像的打印解析度。

設定列印解析度並不會變更回覆影像的像素大小。

## 屬性 {#section-03c7910ebe234804a319e5d0d8ef3a74}

請求屬性。 不論目前的圖層設定為何，都適用。

## 預設 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` 或嵌入源影像中的打印解析度。

## 另請參閱 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[目錄：:PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
