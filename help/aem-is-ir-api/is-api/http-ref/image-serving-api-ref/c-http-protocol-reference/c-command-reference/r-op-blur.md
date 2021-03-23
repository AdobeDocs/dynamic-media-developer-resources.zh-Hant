---
description: 模糊影像。 將模糊濾鏡套用至影像資料。
seo-description: 模糊影像。 將模糊濾鏡套用至影像資料。
seo-title: op_blur
solution: Experience Manager
title: op_blur
uuid: 8405bbb5-fe09-412e-9b52-0af2c01f48b9
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 2%

---


# op_blur{#op-blur}

模糊影像。 將模糊濾鏡套用至影像資料。

`op_blur= *`半徑`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 半徑</span> </p> </td> 
  <td class="stentry"> <p>模糊濾鏡半徑（像素）（實數0..100）。 </p></td> 
 </tr> 
</table>

*`radius`* 是相對於合成影像的像素。也用於羽化圖層效果。

## 屬性 {#section-92573fe2c07746a7bab93a81fc3d208d}

圖層命令。 如果`layer=comp`，則套用至目前圖層或複合影像。

## 預設 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`，以免產生模糊效果。

## 範例 {#section-1ebacde68388492eb108ae0fcd7424db}

模糊影像的背景。 `catalog::MaskPath`會參照個別的遮色片影像。 請注意，必須明確指定`layer=0`，否則`op_blur`將應用於整個複合映像。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
