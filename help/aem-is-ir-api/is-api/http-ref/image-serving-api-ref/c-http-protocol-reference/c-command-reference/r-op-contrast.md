---
description: 調整對比。 增加亮度超過50%的像素亮度，並降低亮度低於50%的像素亮度，以調整影像對比度。
seo-description: 調整對比。 增加亮度超過50%的像素亮度，並降低亮度低於50%的像素亮度，以調整影像對比度。
seo-title: op_contrast
solution: Experience Manager
title: op_contrast
topic: Scene7 Image Serving - Image Rendering API
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_contrast{#op-contrast}

調整對比。 增加亮度超過50%的像素亮度，並降低亮度低於50%的像素亮度，以調整影像對比度。

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>對比度調整(-100...100 int)。 </p></td> 
 </tr> 
</table>

## 屬性 {#section-d319ed55057344eab0a3c93f720acdbf}

圖層命令。 應用於當前圖層或複合影像（如果） `layer=comp`。 被效果圖層忽略。

## 預設 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`，而不會改變對比。 在應用操作之前，CMYK影像或圖層將轉換為RGB。

## 範例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

降低高品質影像圖層的對比度和清晰度，以視覺化方式將它與低品質的背景像片比對：

… `&op_blur=3&op_contrast=-12&`

未來版本可能會使用影像的中值亮度，而非固定的50%亮度。
