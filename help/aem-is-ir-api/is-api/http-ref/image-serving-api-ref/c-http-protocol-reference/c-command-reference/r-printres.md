---
description: 打印解析度。 覆蓋嵌入在響應影像中的打印解析度值。
solution: Experience Manager
title: 打印資源
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# 打印資源{#printres}

打印解析度。 覆蓋嵌入在響應影像中的打印解析度值。

`printRes= *`谷`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 谷</span> </p> </td> 
  <td class="stentry"> <p>打印解析度(dpi)。 </p></td> 
 </tr> 
</table>

打印解析度通常由 `catalog::PrintResolution` 如果是目錄條目，則通過嵌入在源影像中的打印解析度值。 對於模板或分層複合影像，在響應檔案中嵌入的預設打印解析度是具有最低圖層編號的圖層影像的打印解析度。

設定打印解析度不會更改回復影像的像素大小。

## 屬性 {#section-03c7910ebe234804a319e5d0d8ef3a74}

請求屬性。 無論當前圖層設定如何都適用。

## 預設 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` 或源影像中嵌入的打印解析度。

## 另請參閱 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[目錄：:PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
