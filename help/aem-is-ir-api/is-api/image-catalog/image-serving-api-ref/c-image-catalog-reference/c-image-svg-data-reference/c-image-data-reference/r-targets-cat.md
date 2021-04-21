---
description: 縮放目標資料。 無或更多縮放目標屬性，可與縮放檢視器用戶端搭配使用。
solution: Experience Manager
title: 目標
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 2%

---


# 目標{#targets}

縮放目標資料。 無或更多縮放目標屬性，可與縮放檢視器用戶端搭配使用。

在更換「 `??`」記錄終結器Token後，伺服器會響應`req=targets`返回此欄位的內容。

每個縮放目標最多可以關聯4個屬性：

` Target. *``*.frame= *`numframe`*`

` Target. *`數`*.rect= *`字左側、頂部、寬度、高度`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>縮放目標編號(int);縮放目標必須依序連續編號，從1開始。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 幀  </span> </span> </p> </td> 
  <td class="stentry"> <p>可選影格／頁碼，以鎖定回轉或手冊集的特定影格／頁碼；若未針對回轉和手冊檢視器使用指定為0，則預設為0。被縮放檢視器忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 左側，頂部  </span> </span> </p> </td> 
  <td class="stentry"> <p>像素偏移量從影像左上角到縮放目標矩形左上角(int, int);必須為0或更大。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 寬度、高度  </span> </span> </p> </td> 
  <td class="stentry"> <p>縮放目標矩形的像素大小(int、int);必須大於0。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 標籤  </span> </span> </p> </td> 
  <td class="stentry"> <p>文字資料值；可用作縮放目標連結的文字標籤。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>文字資料值；可用來將特定目標資訊傳遞給用戶端，例如SKU值或熱連結URL。 </p> </td> 
 </tr> 
</table>

Target. *`num`*&#x200B;每個縮放目標都需要。rect，而且必須在影像中完全指定矩形。所有其他屬性都是選用的。

*`label`* 並參 *`userData`* 與文字字串本地化。如需詳細資訊，請參閱&#x200B;*HTTP通訊協定參考*&#x200B;中的[文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

對於包含回轉和手冊檢視器用戶端的應用程式，縮放目標必須定義在定義影像集的相同目錄記錄中。 檢視器會忽略影像整合員目錄記錄中的任何縮放目標定義。

Dynamic Media觀看者預期縮放目標位於已經由`catalog::Modifier`命令調整的全解析度影像的坐標中。

## 屬性 {#section-b3f8eba4985f4b00bb935d592fe770f9}

[屬性](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 資料值。

## 預設 {#section-feab29f6575e482391086a57f547543c}

無。

## 另請參閱 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog:::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , catalog::Modifier [, ](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)req= [，文字字串本](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) [地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
