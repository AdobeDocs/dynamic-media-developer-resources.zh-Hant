---
description: 影像集. 指定在生成req=set響應時使用的影像集值。
solution: Experience Manager
title: 影像集
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 8%

---

# 影像集{#imageset}

影像集. 指定在生成req=set響應時使用的影像集值。

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 谷</span></span> </p> </td> 
  <td class="stentry"> <p>影像集字串。 </p></td> 
 </tr> 
</table>

要轉義該值，並確保所有包含的修飾符不被解釋為URL查詢字串的一部分，應將整個值括在花括弧中。 如果在淨路徑中指定目錄記錄，則此修改量值將覆蓋 `catalog::ImageSet` 從主記錄里。 有關有效映像集語法的說明，請參閱 `catalog::ImageSet` 文檔。

## 屬性 {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

請求屬性。 選擇性. 覆蓋 `catalog::ImageSet` 從主記錄開始。

## 預設 {#section-e8622ff40408450fb79d028f8d37fa6b}

無。

## 範例 {#section-68513d3c601f477399602a0741dab390}

指定與一起使用的影像集 `req=set` 請求：

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 另請參閱 {#section-7e0320b2e09d475897082711a8f023a9}

[目錄：:ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) 。 [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。 [媒體集請求](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
