---
description: 調整對比度。 通過增加亮度超過50%的像素的亮度和亮度低於50%的像素的亮度來調整影像對比度。
solution: Experience Manager
title: op_contrast
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# op_contrast{#op-contrast}

調整對比度。 通過增加亮度超過50%的像素的亮度和亮度低於50%的像素的亮度來調整影像對比度。

`op_contrast= *`阿傑`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 阿傑</span> </p> </td> 
  <td class="stentry"> <p>對比度調整(-100..100 int)。 </p></td> 
 </tr> 
</table>

## 屬性 {#section-d319ed55057344eab0a3c93f720acdbf}

層命令。 應用於當前圖層或複合影像 `layer=comp`。 被效果層忽略。

## 預設 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`，對比度不變。 在應用操作之前，CMYK影像或圖層將轉換為RGB。

## 範例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

降低高質量影像圖層的對比度和銳度，使其與低質量背景照片進行視覺匹配：

… `&op_blur=3&op_contrast=-12&`

未來版本可以使用影像的中值亮度，而不是固定的50%亮度。
