---
description: 合成模板。 允許指定位於主目錄以外的目錄中的合成模板。
solution: Experience Manager
title: 範本
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 6%

---

# 範本{#template}

合成模板。 用於在除主目錄外的目錄中指定合成模板。

`template= *`範本`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>範本. </p></td> 
 </tr> 
</table>

*`template`* 必須是包含在 `catalog::Modifier`。

當 `template=` 存在時，請求路徑中指定的對象不會作為層0的源應用。 但是，它可以作為 `src=` 或 `mask=` 使用預定義路徑變數在模板中的任意位置 `$object$` 作為 `src=` 值。 `catalog::Modifier` 在請求路徑中指定的對象的替換僅與 `$object$` 在模板中，而 `catalog::PostModifier` 的子菜單。

層0在模板主體中定義，可以是影像、純色、文本或嵌套或嵌入的請求層。

`catalog:PostModifier` 共 *`object`* 忽略 *`object`* 與 `template=`。

## 預設 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

無。

## 屬性 {#section-daf3afb1d09c45a6a394468d0874c439}

請求屬性。 無論當前圖層設定如何都適用。

## 範例 {#section-9a4f260ed43342b186b0fe855f34bca6}

請參閱中的示例 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另請參閱 {#section-067587444f774469931ecafd5a39834c}

[對象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。 [預定義路徑變數](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
