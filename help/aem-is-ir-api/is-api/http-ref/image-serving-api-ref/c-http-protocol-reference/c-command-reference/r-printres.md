---
title: printRes
description: 列印解析度。 覆寫內嵌在回應影像中的列印解析度值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# printRes{#printres}

列印解析度。 覆寫內嵌在回應影像中的列印解析度值。

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>列印解析度(dpi)。 </p></td> 
 </tr> 
</table>

列印解析度通常由下列定義 `catalog::PrintResolution` 如果是目錄專案，則以內嵌在來源影像中的列印解析度值來表示。 如果是範本或圖層複合影像，回應檔案中內嵌的預設列印解析度是圖層編號最低之圖層影像的列印解析度。

設定列印解析度不會變更回覆影像的畫素大小。

## 屬性 {#section-03c7910ebe234804a319e5d0d8ef3a74}

要求屬性。 不論目前的圖層設定為何，皆會套用。

## 預設 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` 或是內嵌在來源影像中的列印解析度。

## 另請參閱 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog：：PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
