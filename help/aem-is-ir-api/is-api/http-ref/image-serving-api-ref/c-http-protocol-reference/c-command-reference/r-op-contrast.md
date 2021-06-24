---
description: 調整對比度。 通過增加亮度大於50%的像素的亮度，以及減少亮度小於50%的像素的亮度來調整影像對比度。
solution: Experience Manager
title: op_contript
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# op_contript{#op-contrast}

調整對比度。 通過增加亮度大於50%的像素的亮度，以及減少亮度小於50%的像素的亮度來調整影像對比度。

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>對比調整百分比(-100...100 int)。 </p></td> 
 </tr> 
</table>

## 屬性 {#section-d319ed55057344eab0a3c93f720acdbf}

圖層命令。 若`layer=comp`，則套用至目前層或複合影像。 被效果層忽略。

## 預設 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`，對比不會變更。在應用操作之前， CMYK影像或圖層會轉換為RGB。

## 範例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

降低高品質影像層的對比度和銳度，以視覺方式將其與低品質背景照片匹配：

… `&op_blur=3&op_contrast=-12&`

未來版本可能會使用影像的中位亮度，而非固定的50%亮度。
