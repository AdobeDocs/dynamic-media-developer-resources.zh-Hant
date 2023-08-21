---
title: 網路
description: 瞭解如何使用網路頻寬最佳化，根據實際網路頻寬調整影像品質。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 2%

---

# 網路{#network}

開啟網路頻寬會自動根據實際網路頻寬調整影像品質。 對於較差的網路頻寬， [DPR （裝置畫素比率）](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) 最佳化功能會自動關閉，即使它已經開啟。

如有需要，貴公司可透過附加以選擇退出個別影像層級的網路頻寬最佳化 `network=off` 至影像的URL。

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 開啟|關閉 </span> </p> </td> 
  <td class="stentry"> <p>指定網路頻寬是根據實際網路頻寬（開啟）來調整影像品質，或是關閉網路頻寬最佳化以不調整影像品質。</p> </td> 
 </tr> 
</table>

DPR和網路頻寬值是根據偵測到的套件式CDN使用者端值。 這些值有時不準確。 例如，iPhone5搭配 `dpr=2`和iPhone12搭配 `dpr=3`，兩部節目 `dpr=2`. 不過，對於高解析度裝置，傳送 `dpr=2` 比傳送dpr=1好。 然而，克服這種不正確性的最佳方式是使用使用者端DPR，為您提供100%正確的值。 而且它適用於任何裝置，不論是Apple或任何其他已啟動的裝置。 另請參閱 [搭配使用者端裝置畫素比使用智慧型影像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## 屬性



## 預設

`network=off`

## 範例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## 另請參閱

[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md)， [智慧型影像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)