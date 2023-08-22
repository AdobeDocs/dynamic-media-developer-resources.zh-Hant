---
title: 範本
description: 撰寫範本。 允許指定位於主目錄以外的目錄中的合成範本。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 6%

---

# 範本{#template}

撰寫範本。 可讓您在主目錄以外的目錄中指定合成範本。

`template= *`範本`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>範本. </p></td> 
 </tr> 
</table>

*`template`* 必須是包含範本本文中的影像目錄專案 `catalog::Modifier`.

時間 `template=` 存在，請求路徑中指定的物件不會套用為圖層0的來源。 但是，它可以作為 `src=` 或 `mask=` 使用預先定義的路徑變數，在範本中的任一處執行 `$object$` as a `src=` 值。 `catalog::Modifier` 請求路徑中指定的物件的ID僅會套用 `$object$` 在範本內，而 `catalog::PostModifier` 一律會套用。

圖層0是在範本內文中定義的，可以是影像、純色、文字、巢狀或內嵌的要求圖層。

`catalog:PostModifier` 之 *`object`* 忽略於 *`object`* 搭配使用 `template=`.

## 預設 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

無。

## 屬性 {#section-daf3afb1d09c45a6a394468d0874c439}

要求屬性。 不論目前的圖層設定為何，皆會套用。

## 範例 {#section-9a4f260ed43342b186b0fe855f34bca6}

請參閱下列範例： [範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 另請參閱 {#section-067587444f774469931ecafd5a39834c}

[物件](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)， [範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)， [預先定義的路徑變數](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
