---
description: 縮放目標資料。 無或更多縮放目標屬性，可與縮放檢視器用戶端搭配使用。
seo-description: 縮放目標資料。 無或更多縮放目標屬性，可與縮放檢視器用戶端搭配使用。
seo-title: 目標
solution: Experience Manager
title: 目標
topic: Scene7 Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# 目標{#targets}

縮放目標資料。 無或更多縮放目標屬性，可與縮放檢視器用戶端搭配使用。

在更換「 」記錄終結器標籤後，服 `req=targets`務器返回此 `??`欄位的內容。

每個縮放目標最多可以關聯4個屬性：

` Target. *``*.frame= *`numframe`*`

` Target. *`數`*.rect= *`字左側、頂部、寬度、高度`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 數 </span></span> </p> </td> 
  <td class="stentry"> <p>縮放目標編號(int);縮放目標必須依序連續編號，從1開始。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 框架 </span></span> </p> </td> 
  <td class="stentry"> <p>可選影格／頁碼，以鎖定回轉或手冊集的特定影格／頁碼；若未針對回轉和手冊檢視器使用指定為0，則預設為0。被縮放檢視器忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 左側，頂部 </span></span> </p> </td> 
  <td class="stentry"> <p>像素偏移量從影像左上角到縮放目標矩形左上角(int, int);必須為0或更大。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 寬度、高度 </span></span> </p> </td> 
  <td class="stentry"> <p>縮放目標矩形的像素大小(int、int);必須大於0。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 標籤 </span></span> </p> </td> 
  <td class="stentry"> <p>文字資料值；可用作縮放目標連結的文字標籤。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 使 <span class="varname"> 用者資 </span> 料 </span> </p> </td> 
  <td class="stentry"> <p>文字資料值；可用來將特定目標資訊傳遞給用戶端，例如SKU值或熱連結URL。 </p> </td> 
 </tr> 
</table>

Target. *`num`*&#x200B;每個縮放目標都需要。rect，而且必須在影像中完全指定矩形。 所有其他屬性都是選用的。

*`label`* 並參 *`userData`* 與文字字串本地化。 如需詳細 [資訊，請參閱](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)*HTTP通訊協定參考中的文字字串本地化* 。

對於包含回轉和手冊檢視器用戶端的應用程式，縮放目標必須定義在定義影像集的相同目錄記錄中。 檢視器會忽略影像整合員目錄記錄中的任何縮放目標定義。

Scene7檢視器預期縮放目標會位於已由命令調整的完整解析度影像的座標中 `catalog::Modifier`。

## 屬性 {#section-b3f8eba4985f4b00bb935d592fe770f9}

[屬性資料](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 值。

## 預設 {#section-feab29f6575e482391086a57f547543c}

無。

## 另請參閱 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog:::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , catalog::Modifier [,](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)req= [，文字字串本](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)[地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
