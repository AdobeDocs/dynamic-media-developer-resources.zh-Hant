---
title: dpr
description: 裝置畫素比率(DPR)&mdash；也稱為CSS畫素比率&mdash；是裝置的實體畫素與邏輯畫素之間的關係。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---

# dpr{#dpr}

裝置畫素比率(DPR) （也稱為CSS畫素比率）是裝置的實體畫素與邏輯畫素之間的關係。 特別是隨著Retina熒幕的出現，現代行動裝置的畫素解析度正以快速的速度增長。

啟用「裝置畫素比最佳化」 ，以熒幕的原生解析度呈現影像，使影像更清晰。

目前，顯示器的畫素密度來自Akamai CDN標題值。

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 關閉 </span> </span> </p> </td> 
  <td class="stentry"> <p>關閉個別影像URL層級的DPR最佳化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 開啟，dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>使用自訂值（任何使用者端邏輯或其他方式偵測到的值）覆寫智慧型影像偵測到的DPR值。 dprValue的允許值是大於0的任何數字。 </p> </td> 
 </tr> 
</table>


您可以使用 `dpr=on,dprValue` 即使公司層級DPR設為關閉。

由於DPR最佳化，當產生的影像大於MaxPix Dynamic Media設定時，一律會透過維持影像的外觀比例來辨識MaxPix寬度。

| 要求的影像大小 | DPR值 | 傳遞的影像大小 |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

## 屬性



## 預設

`dpr=off`


## 範例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## 另請參閱

[網路](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md)， [智慧型影像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)