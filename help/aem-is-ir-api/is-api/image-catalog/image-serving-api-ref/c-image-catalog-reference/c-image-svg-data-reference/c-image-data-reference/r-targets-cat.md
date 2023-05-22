---
description: 縮放目標資料。 無或更多縮放目標屬性，這些屬性可與縮放查看器客戶端結合使用。
solution: Experience Manager
title: 目標
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 2%

---

# 目標{#targets}

縮放目標資料。 無或更多縮放目標屬性，這些屬性可與縮放查看器客戶端結合使用。

伺服器返回此欄位的內容以響應 `req=targets`，在替換「後 `??`&#39;記錄終結器標籤。

每個縮放目標最多可以關聯四個屬性：

` Target. *`數`*.frame= *`幀`*`

` Target. *`數`*.rect= *`左，上，寬，高`*`

` Target. *`數`*.label= *`標籤`*`

` Target. *`數`*.userData= *`用戶資料`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 數 </span> </span> </p> </td> 
  <td class="stentry"> <p>縮放目標編號(int);縮放目標必須按順序和連續編號，從1開始。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 幀 </span> </span> </p> </td> 
  <td class="stentry"> <p>可選幀/頁碼，用於針對旋轉或手冊集的特定幀/頁；如果未指定用於旋轉和手冊瀏覽器，則預設為0;被縮放查看器忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 左，上 </span> </span> </p> </td> 
  <td class="stentry"> <p>從影像左上角到縮放目標矩形左上角的像素偏移(int、int);必須為0或更大。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 寬度，高度 </span> </span> </p> </td> 
  <td class="stentry"> <p>縮放目標矩形的像素大小(int、int);必須大於0。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 標籤 </span> </span> </p> </td> 
  <td class="stentry"> <p>文本資料值；可用作縮放目標連結的文本標籤。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 用戶資料 </span> </span> </p> </td> 
  <td class="stentry"> <p>文本資料值；可能用於將特定於目標的資訊傳遞給客戶端，如SKU值或熱連結URL。 </p> </td> 
 </tr> 
</table>

Target. *`num`*&#x200B;每個縮放目標都需要.rect，並且必須在影像中指定一個完全矩形。 所有其它屬性都是可選的。

*`label`* 和 *`userData`* 參與文本字串本地化。 請參閱 [文本字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 的 *HTTP協定引用* 的雙曲餘切值。

對於涉及旋轉和手冊瀏覽器客戶端的應用程式，縮放目標必須定義在定義影像集的同一目錄記錄中。 查看器將忽略影像整合員的目錄記錄中的任何縮放目標定義。

Dynamic Media觀眾期望在已經由來自的命令調整的全解析度影像的坐標中縮放目標 `catalog::Modifier`。

## 屬性 {#section-b3f8eba4985f4b00bb935d592fe770f9}

[屬性資料](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 值。

## 預設 {#section-feab29f6575e482391086a57f547543c}

無。

## 另請參閱 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[目錄：:ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) 。 [目錄：：修改量](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)。 [請求=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)。 [文本字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
