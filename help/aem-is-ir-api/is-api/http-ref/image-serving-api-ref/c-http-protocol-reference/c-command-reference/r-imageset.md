---
description: 影像集. 指定在生成req=set響應時要使用的影像集值。
seo-description: 影像集. 指定在生成req=set響應時要使用的影像集值。
seo-title: imageSet
solution: Experience Manager
title: imageSet
topic: Scene7 Image Serving - Image Rendering API
uuid: ecfb3905-e3ef-4ab8-a2c4-2c3f200e0f0f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# imageSet{#imageset}

影像集. 指定在生成req=set響應時要使用的影像集值。

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>影像集字串。 </p></td> 
 </tr> 
</table>

若要逸出值，並確保所有包含的修飾元未解譯為URL查詢字串的一部分，則整個值應以大括弧括住。 如果在淨路徑中指定目錄記錄，則此修改量值會從主 `catalog::ImageSet` 記錄中覆寫。 如需有效影像集語法的說明，請參閱文 `catalog::ImageSet` 件。

## 屬性 {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

請求屬性。 選填。從主 `catalog::ImageSet` 記錄覆寫。

## 預設 {#section-e8622ff40408450fb79d028f8d37fa6b}

無。

## 範例 {#section-68513d3c601f477399602a0741dab390}

指定影像集以搭配請求使 `req=set` 用：

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 另請參閱 {#section-7e0320b2e09d475897082711a8f023a9}

[目錄：:ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) 、 [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、媒體集請 [求](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
