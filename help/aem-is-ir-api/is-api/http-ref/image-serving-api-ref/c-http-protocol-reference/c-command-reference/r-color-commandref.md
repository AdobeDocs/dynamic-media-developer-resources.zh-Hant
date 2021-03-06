---
title: 色彩
description: 圖層顏色。 指定實色和效果圖層的前景色和不透明度，以及文本框填充文本圖層的顏色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 4%

---

# 色彩{#color}

圖層顏色。 指定實色和效果圖層的前景色和不透明度，以及文本框填充文本圖層的顏色。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 顏色 </span> </span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK顏色值，帶或不帶Alpha。 </p> </td> 
 </tr> 
</table>

對於影像和文本圖層， `color=` 用指定顏色*填充圖層的邊界矩形內的透明和半不透明區域 `rotate=` 和 `extend=` 的子菜單。

## 屬性 {#section-d6e74c36a49547849212e4db8927e678}

層屬性。 應用於當前圖層，如果 `layer=comp`。

*`color`* 假設存在於對應於像素類型的工作顏色空間中 *`color`*。 *`color`* 如果圖層影像在合併時具有不同的像素類型，則精確轉換。

## 預設 {#section-60611c72876b4c45b5c85ce35608e5ec}

無固色和效果圖層的預設值；必須指定顏色。 影像和文本圖層的預設值為0,0,0,0（完全透明）。

## 範例 {#section-2d090493f4ec4e188bbc5565aa151a05}

在以下模板片段中，我們將文本背景設定為50%的不透明顏色，並使用相同顏色在第2層影像周圍添加半透明的10像素邊框：

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 另請參閱 {#section-f0e059f857b64b61ab4f23312b8dc619}

[顏色](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)。 [bg顏色=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)。 [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)。 [擴展=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)。 [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)。 [色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
