---
description: 戴卡尺寸。 傾斜材質物件的寬度、高度和厚度。
solution: Experience Manager
title: 大小
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 5%

---


# 大小{#size}

戴卡尺寸。 傾斜材質物件的寬度、高度和厚度。

## 屬性 {#section-967bf1112eec4032a91ed0c8a7b10a07}

以逗號分隔的三個實數。 不得為負面。 將未使用的值設定為0。 可省略尾隨零。

只有在影像應拉伸以符合指定大小（長寬比可能會變更）時，才指定寬度和高度。 設定寬度或高度，以按比例縮放影像。 將寬度和高度都設定為0，以使用`catalog::Resolution`確定對象大小。

提供厚度值，以將陰影加入貼花物件。 對於傾斜材料是可選的，被所有其他材料忽略。

## 預設 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

萬，萬。 這表示要根據目錄：:Resolution來決定貼花大小，且物件沒有厚度（因此不會產生下垂式陰影）。

## 範例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>貼花板會強制尺寸為12x3英吋，且無厚度（即無下垂式陰影）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>傾斜寬度為5英吋，高度由影像的長寬比確定，並基於1英吋厚度產生陰影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>傾斜寬度和高度由目錄：：解析度確定，厚度為半英吋。 </p></td> 
 </tr> 
</table>

## 另請參閱 {#section-31a164e781d14e92bd9d379d3c329e92}

[目錄：：解析度](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
