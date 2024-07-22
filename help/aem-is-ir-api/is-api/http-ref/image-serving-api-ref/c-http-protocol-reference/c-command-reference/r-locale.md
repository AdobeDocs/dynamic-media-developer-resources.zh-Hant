---
title: 地區設定
description: 翻譯地區設定Id。 指定要求的地區設定ID。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# 地區設定{#locale}

翻譯地區設定Id。 指定要求的地區設定ID。

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>地區ID （字串）。 </p></td> 
 </tr> 
</table>

使用此ID以及以`attribute::LocaleMap`和`attribute::LocaleStrMap`指定的規則，「影像伺服」會套用選用的目錄ID轉譯和字串本地化。

## 屬性 {#section-1854a9902b884d9b8e8e713b6635723f}

要求命令。 套用至整個請求，包括巢狀/內嵌請求，無論其指定的位置為何。 `locId`只能包含可列印的ASCII字元。 若未在此要求的主目錄中定義本地化地圖，則忽略。 如果指定了空白或無效的`locId`，而且在`attribute::DefaultLocale`中未定義預設規則，則會傳回錯誤。

## 預設 {#section-9699fbc26de6453e9029e0003c79a7ef}

未指定locale=時使用`attribute::DefaultLocale`。

## 另請參閱 {#section-28a586d43ac4429d98e318a580c92af4}

[attribute：：DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) ， [attribute：：LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)， [attribute：：LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)，本地化支援
