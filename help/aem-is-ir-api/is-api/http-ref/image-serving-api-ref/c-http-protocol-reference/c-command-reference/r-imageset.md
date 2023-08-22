---
title: imageSet
description: 影像集. 指定產生req=set回應時使用的影像集值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 8%

---

# imageSet{#imageset}

影像集. 指定產生req=set回應時使用的影像集值。

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>影像集字串。 </p></td> 
 </tr> 
</table>

若要逸出值並確保任何包含的修飾詞都不會解譯為URL查詢字串的一部分，整個值應以大括弧括住。 如果在網路路徑中指定了目錄記錄，則此修飾元值會覆寫 `catalog::ImageSet` 從主要記錄。 如需有效影像集語法的說明，請參閱 `catalog::ImageSet` 檔案。

## 屬性 {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

要求屬性。 選擇性. 覆寫 `catalog::ImageSet` 從主要記錄。

## 預設 {#section-e8622ff40408450fb79d028f8d37fa6b}

無。

## 範例 {#section-68513d3c601f477399602a0741dab390}

指定要搭配使用的影像集 `req=set` 要求：

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 另請參閱 {#section-7e0320b2e09d475897082711a8f023a9}

[catalog：：ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) ， [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)， [媒體集要求](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
