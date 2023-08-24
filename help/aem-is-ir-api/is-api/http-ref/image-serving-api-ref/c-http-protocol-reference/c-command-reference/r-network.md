---
title: 網路
description: 瞭解如何使用網路頻寬最佳化，根據實際網路頻寬調整影像品質。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: a6e0db8238ba5f2209089c6eda7b42c42f66b25f
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 3%

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

網路頻寬值是以偵測到的套件式CDN使用者端值為基礎。

## 屬性

要求屬性。 如果網路狀況良好，則不會有任何效果。

## 預設

`network=off`

## 範例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## 另請參閱

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md)， [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md)， [智慧型影像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)