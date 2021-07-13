---
description: 傾斜大小。 傾倒材料對象的寬度、高度和厚度。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 5%

---

# 大小{#size}

傾斜大小。 傾倒材料對象的寬度、高度和厚度。

## 屬性 {#section-967bf1112eec4032a91ed0c8a7b10a07}

三個實數以逗號分隔。 不得為負。 將未使用的值設定為0。 尾隨零可忽略。

只有在影像應拉伸以符合指定大小時，才指定寬度和高度（外觀比例可能改變）。 設定寬度或高度以按比例縮放影像。 將寬度和高度設定為0以使用`catalog::Resolution`確定對象大小。

提供厚度值，以將陰影添加到陰影對象。 可選，由所有其他材料忽略。

## 預設 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

一萬。 這表示將根據目錄：：解析度來確定傾斜大小，並且對象沒有厚度（因此不會呈現投影）。

## 範例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>傾斜板的尺寸被強制為12x3英吋，且無厚度（即無陰影）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>該陰影寬5英吋，高度由影像的長寬比確定，並且基於1英吋厚度來呈現陰影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>傾斜寬度和高度由目錄：：解析度決定，為1/2英吋厚。 </p></td> 
 </tr> 
</table>

## 另請參閱 {#section-31a164e781d14e92bd9d379d3c329e92}

[目錄：：解析度](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
