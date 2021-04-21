---
description: 調整飽和度。 變更圖層或複合影像中每個可見像素的飽合度。
solution: Experience Manager
title: op_saturation
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---


# op_saturation{#op-saturation}

調整飽和度。 變更圖層或複合影像中每個可見像素的飽合度。

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>飽和度調整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

`op_saturation=-100` 完全去除影像的飽和度。

## 屬性 {#section-9a3cc9ff060049449554dfa69d92fd53}

圖層命令。 如果`layer=comp`，則套用至目前圖層或複合影像。 被效果圖層忽略。

## 預設 {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`，以保持飽和度不變。在應用操作之前，CMYK影像或圖層將轉換為RGB。

## 範例 {#section-033b272f1b7e4efeb94e841fd8095357}

操控彩色像片以呈現「高關鍵」外觀：

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
