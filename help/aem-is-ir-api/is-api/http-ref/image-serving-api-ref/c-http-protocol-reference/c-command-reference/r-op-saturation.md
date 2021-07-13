---
description: 調整飽和度。 更改圖層或複合影像的每個可見像素的飽和度。
solution: Experience Manager
title: op_saturation
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# op_saturation{#op-saturation}

調整飽和度。 更改圖層或複合影像的每個可見像素的飽和度。

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>飽和度調整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

`op_saturation=-100` 影像會完全去飽和。

## 屬性 {#section-9a3cc9ff060049449554dfa69d92fd53}

圖層命令。 若`layer=comp`，則套用至目前層或複合影像。 被效果層忽略。

## 預設 {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`，以保持飽和度不變。在應用操作之前， CMYK影像或圖層會轉換為RGB。

## 範例 {#section-033b272f1b7e4efeb94e841fd8095357}

操控彩色照片以獲得「高關鍵」外觀：

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
