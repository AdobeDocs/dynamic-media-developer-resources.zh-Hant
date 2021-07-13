---
description: 將影像與視圖對齊。 在由wid=和hei=定義的視圖矩形內對齊複合影像（如果也指定了scl=，則可能在縮放後）。
solution: Experience Manager
title: 對齊
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---

# 對齊{#align}

將影像與視圖對齊。 在由wid=和hei=定義的視圖矩形內對齊複合影像（如果也指定了scl=，則可能在縮放後）。

` align= *``*, *`horizvert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 霍里茲  </span> </span> </p> </td> 
  <td class="stentry"> <p>水準對齊（實數， -1.0...1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 變態  </span> </span> </p> </td> 
  <td class="stentry"> <p>垂直對齊（實數， -1.0...1.0） </p> </td> 
 </tr> 
</table>

指定`align=-1,-1`將複合影像的左上角與視圖的左上角對齊，指定`align=1,1`將影像的右下角與視圖的右下角對齊。 對於標準影像和縮圖請求，複合影像資料未覆蓋的檢視任何區域都會填入`bgc=`。

## 屬性 {#section-3fbec8206fc944eda4746d8be84f3b41}

檢視屬性。 （`align=`還用於定義水印影像和應用水印的複合影像之間的對齊方式。） 無論目前的層設定為何皆適用。 如果只指定`wid=`和`hei=`中的一個，並且`fit=constrain`或`fit=stretch`時，則忽略。

## 預設 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`，可將影像在視圖矩形中居中。

## 範例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

以下請求適用於200x200像素視圖矩形中的`myImage`。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

如果`myImage`正方形，則填充整個視圖矩形。 如果`myImage`有縱向長寬比，則會縮放為200像素高，並在檢視中水準居中。 如果`myImage`具有橫向長寬比，則縮放為200像素寬，並與視圖的頂邊對齊。 在所有情況下，傳回的影像大小都恰好為200x200像素；縮放`myImage`未覆蓋的任何空間都填充`attribute::BkgColor`（指定bgc=以動態控制背景顏色）。

## 另請參閱 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), fit= [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [水印](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
