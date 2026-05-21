---
title: 網路
description: 瞭解如何使用網路頻寬最佳化，根據實際網路頻寬調整影像品質。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
TQID: 'https://experienceleague.adobe.com/9odHf3s93xaQyc1WSkXGamAgoQP070p7ItB9HhyT-dQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 3%

---

# 網路{#network}

開啟網路頻寬會自動根據實際網路頻寬調整影像品質。 因為網路頻寬太低，[DPR （裝置畫素比例）](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md)最佳化功能會自動關閉，即使它已經開啟。

如有需要，貴公司可將`network=off`附加至影像的URL，選擇退出個別影像層級的網路頻寬最佳化。

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">開啟|關閉</span> </p> </td> 
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

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md)，[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md)，[智慧型影像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
