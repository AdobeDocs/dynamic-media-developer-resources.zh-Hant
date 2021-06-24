---
description: 模糊影像。 對影像資料套用模糊篩選。
solution: Experience Manager
title: op_blur
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# op_blur{#op-blur}

模糊影像。 對影像資料套用模糊篩選。

`op_blur= *`半徑`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 半徑</span> </p> </td> 
  <td class="stentry"> <p>模糊濾鏡半徑（像素）（實數0.100）。 </p></td> 
 </tr> 
</table>

*`radius`* 是相對於複合影像的像素。也用於羽化圖層效果。

## 屬性 {#section-92573fe2c07746a7bab93a81fc3d208d}

圖層命令。 若`layer=comp`，則套用至目前層或複合影像。

## 預設 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`，無模糊效果。

## 範例 {#section-1ebacde68388492eb108ae0fcd7424db}

模糊影像的背景。 `catalog::MaskPath`引用單獨的蒙版影像。 請注意，必須明確指定`layer=0`，否則，將將`op_blur`應用於整個複合映像。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
