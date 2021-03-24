---
description: 影像集. 指定在生成req=set響應時要使用的影像集值。
solution: Experience Manager
title: imageSet
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 8%

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

若要逸出值，並確保所有包含的修飾元未解譯為URL查詢字串的一部分，則整個值應以大括弧括住。 如果在淨路徑中指定目錄記錄，則此修飾詞值會從主記錄覆寫`catalog::ImageSet`。 有關有效映像集語法的說明，請參閱`catalog::ImageSet`文檔。

## 屬性 {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

請求屬性。 選填。從主記錄覆寫`catalog::ImageSet`。

## 預設 {#section-e8622ff40408450fb79d028f8d37fa6b}

無。

## 範例 {#section-68513d3c601f477399602a0741dab390}

指定影像集以搭配`req=set`請求使用：

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 另請參閱 {#section-7e0320b2e09d475897082711a8f023a9}

[目錄：:ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) 、 [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、媒體集 [請求](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
