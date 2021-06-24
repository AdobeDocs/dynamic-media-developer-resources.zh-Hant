---
description: 合成範本。 允許指定位於主目錄以外的目錄中的合成模板。
solution: Experience Manager
title: 範本
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 6%

---

# 範本{#template}

合成範本。 可讓您在主目錄以外的目錄中指定複合範本。

`template= *`範本`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>範本. </p></td> 
 </tr> 
</table>

*`template`* 必須是包含範本內文的影像目錄項 `catalog::Modifier`目。

當`template=`存在時，在請求路徑中指定的對象不會應用為層0的源。 不過，透過使用預先定義的路徑變數`$object$`作為`src=`值，該變數在範本中的任何位置都可以參照為`src=`或`mask=`。 `catalog::Modifier` 在請求路徑中指定的物件，只會套用範本內 `$object$` 的替代，而 `catalog::PostModifier` 一律會套用。

第0層定義於範本內文中，可以是影像、實色、文字或巢狀或內嵌的請求層。

`catalog:PostModifier` 搭配 *`object`* 使用時 *`object`* 會忽略 `template=`。

## 預設 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

無。

## 屬性 {#section-daf3afb1d09c45a6a394468d0874c439}

要求屬性。 無論目前的層設定為何，都適用。

## 範例 {#section-9a4f260ed43342b186b0fe855f34bca6}

請參閱[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的範例。

## 另請參閱 {#section-067587444f774469931ecafd5a39834c}

[物件](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、范 [本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、預先定 [義的路徑變數](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
