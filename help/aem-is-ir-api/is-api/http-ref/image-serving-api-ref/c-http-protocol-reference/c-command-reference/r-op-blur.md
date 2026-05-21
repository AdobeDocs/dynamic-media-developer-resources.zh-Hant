---
title: op_blur
description: 模糊影像。 將模糊濾鏡套用至影像資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
TQID: 'https://experienceleague.adobe.com/e7GXc5NYZC2Flk0Uf71iw-hi-gPdQk-XldMpPH-DwqM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 2%

---

# op_blur{#op-blur}

模糊影像。 將模糊濾鏡套用至影像資料。

`op_blur= *`半徑`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">半徑</span> </p> </td> 
  <td class="stentry"> <p>模糊濾鏡半徑，以畫素為單位（實數0..100）。 </p></td> 
 </tr> 
</table>

*`radius`*&#x200B;是相對於複合影像的畫素。 也可用來羽化圖層效果。

## 屬性 {#section-92573fe2c07746a7bab93a81fc3d208d}

圖層指令。 套用至目前的圖層或複合影像（若為`layer=comp`）。

## 預設 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`，沒有模糊效果。

## 範例 {#section-1ebacde68388492eb108ae0fcd7424db}

模糊影像的背景。 `catalog::MaskPath`參考了個別的遮色片影像。 請注意，必須明確指定`layer=0`，否則會將`op_blur`套用至整個複合影像。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
