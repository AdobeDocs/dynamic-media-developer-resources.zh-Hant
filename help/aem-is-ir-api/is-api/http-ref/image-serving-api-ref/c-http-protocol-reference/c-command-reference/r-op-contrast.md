---
description: 調整對比。 增加亮度超過50%的像素亮度，並降低亮度低於50%的像素亮度，以調整影像對比度。
solution: Experience Manager
title: op_contrast
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

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

圖層命令。 如果`layer=comp`，則套用至目前圖層或複合影像。 被效果圖層忽略。

## 預設 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`，而不會改變對比。在應用操作之前，CMYK影像或圖層將轉換為RGB。

## 範例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

降低高品質影像圖層的對比度和清晰度，以視覺化方式將它與低品質背景像片比對：

… `&op_blur=3&op_contrast=-12&`

未來版本可能會使用影像的中值亮度，而非固定的50%亮度。
