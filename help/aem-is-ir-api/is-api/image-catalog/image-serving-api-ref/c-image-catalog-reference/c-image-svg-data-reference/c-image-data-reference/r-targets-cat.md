---
description: 縮放目標資料。 無或更多縮放目標屬性，這些屬性可與縮放查看器客戶端一起使用。
solution: Experience Manager
title: 目標
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 2%

---

# 目標{#targets}

縮放目標資料。 無或更多縮放目標屬性，這些屬性可與縮放查看器客戶端一起使用。

在替換「 `??`」記錄終結器令牌後，伺服器返回此欄位的內容以響應`req=targets`。

最多四個屬性可與每個縮放目標相關聯：

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`數字左，頂，寬，高`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>縮放目標編號（整數）;縮放目標必須從1開始，以順序和連續方式編號。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 框架  </span> </span> </p> </td> 
  <td class="stentry"> <p>可選幀/頁碼，用於鎖定回轉或手冊集的特定幀/頁；若未指定供回轉和手冊檢視器使用，則預設為0;被縮放檢視器忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 左，上  </span> </span> </p> </td> 
  <td class="stentry"> <p>從影像左上角到縮放目標矩形左上角的像素偏移量(int、int);必須為0或更高。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 寬度、高度  </span> </span> </p> </td> 
  <td class="stentry"> <p>縮放目標矩形的像素大小(int、int);必須大於0。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 標籤  </span> </span> </p> </td> 
  <td class="stentry"> <p>文本資料值；可作為縮放目標連結的文字標籤。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>文本資料值；可用來傳遞目標特定資訊給用戶端，例如SKU值或熱連結URL。 </p> </td> 
 </tr> 
</table>

Target. *`num`*&#x200B;每個縮放目標都需要.rect ，必須在影像中完全指定矩形。所有其他屬性均為選用。

*`label`* 並參 *`userData`* 與文字串本地化。如需詳細資訊，請參閱&#x200B;*HTTP通訊協定參考*&#x200B;中的[文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

對於涉及回轉和手冊檢視器用戶端的應用程式，縮放目標必須在定義影像集的相同目錄記錄中定義。 檢視器會忽略影像整合員的目錄記錄中的任何縮放目標定義。

Dynamic Media檢視器會在已經由`catalog::Modifier`命令調整的全解析度影像的座標中預期縮放目標。

## 屬性 {#section-b3f8eba4985f4b00bb935d592fe770f9}

[屬性](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 資料值。

## 預設 {#section-feab29f6575e482391086a57f547543c}

無。

## 另請參閱 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ,  [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834),  [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)，文字字串本地 [化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
