---
title: dpr
description: 裝置畫素比率(DPR)&amp；mdash；也稱為CSS畫素比率&amp；mdash；是裝置的實體畫素與邏輯畫素之間的關係。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d64ca9ed-7d8e-4a13-9c9d-acb7de3e31ed
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 2%

---

# dpr{#dpr}

裝置畫素比率(DPR) （也稱為CSS畫素比率）是裝置的實體畫素與邏輯畫素之間的關係。 特別是隨著Retina熒幕的出現，現代行動裝置的畫素解析度正以快速的速度增長。

啟用「裝置畫素比最佳化」 ，以熒幕的原生解析度呈現影像，使影像更清晰。

目前，顯示器的畫素密度來自Akamai CDN標題值。

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">折扣</span> </span> </p> </td> 
  <td class="stentry"> <p>關閉個別影像URL層級的DPR最佳化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">於，dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>使用自訂值（任何使用者端邏輯或其他方式偵測到的值）覆寫智慧型影像偵測到的DPR值。 dprValue的允許值是大於0的任何數字。 </p> </td> 
 </tr> 
</table>


即使公司層級DPR設定為off，您仍可使用`dpr=on,dprValue`。

由於DPR最佳化，當產生的影像大於MaxPix Dynamic Media設定時，一律會透過維持影像的外觀比例來辨識MaxPix寬度。

| 要求的影像大小 | DPR值 | 傳遞的影像大小 |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

DPR值是根據偵測到的套件式CDN使用者端值。 這些值有時不準確。 例如，具有`dpr=2`的iPhone5和具有dpr=3的iPhone12都顯示`dpr=2`。 不過，對於高解析度裝置，傳送`dpr=2`還是比傳送`dpr=1`好。 然而，克服這種不正確性的最佳方式是使用使用者端DPR，為您提供100%正確的值。 而且它適用於任何裝置，不論是Apple或任何其他已啟動的裝置。 請參閱[使用智慧型影像搭配使用者端裝置畫素比率](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=zh-Hant)。

## 屬性

要求屬性。 如果`dpr`已關閉或`dprValue=1`，則沒有任何效果。

## 預設

`dpr=off`


## 範例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## 另請參閱

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md)，[網路](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md)，[智慧型影像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=zh-Hant)
