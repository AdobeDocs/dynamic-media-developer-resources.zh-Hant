---
description: 翻譯區域設定ID。 指定請求的區域設定ID。
solution: Experience Manager
title: 地區設定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# 地區設定{#locale}

翻譯區域設定ID。 指定請求的區域設定ID。

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>區域設定ID（字串）。 </p></td> 
 </tr> 
</table>

使用此ID和指定的規則 `attribute::LocaleMap` 和 `attribute::LocaleStrMap`，影像服務應用可選目錄ID轉換和字串本地化。

## 屬性 {#section-1854a9902b884d9b8e8e713b6635723f}

請求命令。 應用於整個請求，包括嵌套/嵌入式請求，而不管其指定位置。 `locId` 必須只包含可打印的ASCII字元。 如果此請求的主目錄中未定義本地化映射，則忽略該映射。 如果為空或無效，則返回錯誤 `locId` 是指定的，且未在中定義預設規則 `attribute::DefaultLocale`。

## 預設 {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` 在未指定locale=時使用。

## 另請參閱 {#section-28a586d43ac4429d98e318a580c92af4}

[屬性：:DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) 。 [屬性：:LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)。 [屬性：:LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)，本地化支援
