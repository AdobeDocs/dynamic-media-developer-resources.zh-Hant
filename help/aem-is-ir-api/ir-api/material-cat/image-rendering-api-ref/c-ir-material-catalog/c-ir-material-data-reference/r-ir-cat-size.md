---
description: 德卡爾大小。 傾斜材料對象的寬度、高度和厚度。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 4%

---

# 大小{#size}

德卡爾大小。 傾斜材料對象的寬度、高度和厚度。

## 屬性 {#section-967bf1112eec4032a91ed0c8a7b10a07}

三個實數，用逗號分隔。 不得為負。 將未使用的值設定為0。 可省略尾隨零。

僅當影像應拉伸以適合指定大小時（長寬比可能更改），才指定寬度和高度。 設定寬度或高度以按比例縮放影像。 將寬度和高度均設定為0以使用 `catalog::Resolution`確定對象大小。

提供厚度值，以向貼花對象添加投影。 對於傾斜材料，可選，被所有其他材料忽略。

## 預設 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. 這表示將根據目錄：:Resolution確定貼花大小，並且對象沒有厚度（因此，不呈現投影）。

## 範例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>貼花板被強制尺寸為12x3英吋，且無厚度（即無投影）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>該貼片寬5英吋，高度由影像的長寬比確定，並且基於1英吋厚度渲染投影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>傾斜寬度和高度由目錄：：解析度確定，厚度為1/2英吋。 </p></td> 
 </tr> 
</table>

## 另請參閱 {#section-31a164e781d14e92bd9d379d3c329e92}

[目錄：：解析](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
