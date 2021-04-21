---
description: 構圖範本。 允許指定位於主目錄以外的目錄中的合成模板。
solution: Experience Manager
title: 範本
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 6%

---


# 範本{#template}

構圖範本。 可讓您在目錄中指定除主目錄以外的合成範本。

`template= *`範本`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>範本. </p></td> 
 </tr> 
</table>

*`template`* 必須是包含範本內文的影像目錄項目 `catalog::Modifier`。

當`template=`存在時，在請求路徑中指定的對象不會作為第0層的源應用。 但是，使用預先定義的路徑變數`$object$`作為`src=`值，可將其引用為範本中的任何位置。 `src=``mask=``catalog::Modifier` 在請求路徑中指定的對象，只會以範本中的替 `$object$` 代來套用，而 `catalog::PostModifier` 一律套用。

圖層0定義在範本內文中，可以是影像、純色、文字或巢狀或內嵌的請求圖層。

`catalog:PostModifier` 的 *`object`* 值會在 *`object`* 搭配使用時忽略 `template=`。

## 預設 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

無。

## 屬性 {#section-daf3afb1d09c45a6a394468d0874c439}

請求屬性。 不論目前的圖層設定為何，都適用。

## 範例 {#section-9a4f260ed43342b186b0fe855f34bca6}

請參閱[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的範例。

## 另請參閱 {#section-067587444f774469931ecafd5a39834c}

[物件](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、范 [本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、預先定 [義路徑變數](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
