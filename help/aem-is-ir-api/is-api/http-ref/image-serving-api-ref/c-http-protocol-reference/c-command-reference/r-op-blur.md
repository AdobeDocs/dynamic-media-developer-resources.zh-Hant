---
description: 模糊影像。 將模糊濾鏡套用至影像資料。
seo-description: 模糊影像。 將模糊濾鏡套用至影像資料。
seo-title: op_blur
solution: Experience Manager
title: op_blur
topic: Scene7 Image Serving - Image Rendering API
uuid: 8405bbb5-fe09-412e-9b52-0af2c01f48b9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

*`radius`* 是相對於合成影像的像素。 也用於羽化圖層效果。

## 屬性 {#section-92573fe2c07746a7bab93a81fc3d208d}

圖層命令。 應用於當前圖層或複合影像（如果） `layer=comp`。

## 預設 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`，以免產生模糊效果。

## 範例 {#section-1ebacde68388492eb108ae0fcd7424db}

模糊影像的背景。 參考單獨的遮色片影像 `catalog::MaskPath`。 請注意， `layer=0`必須明確指定，否 `op_blur` 則將應用於整個複合映像。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
