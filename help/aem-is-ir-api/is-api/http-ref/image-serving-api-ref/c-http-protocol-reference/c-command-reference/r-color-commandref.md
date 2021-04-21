---
description: 圖層顏色。 指定純色和效果圖層的前景色和不透明度，並且文字方塊會填滿文字圖層的顏色。
solution: Experience Manager
title: 色彩
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---


# color{#color}

圖層顏色。 指定純色和效果圖層的前景色和不透明度，並且文字方塊會填滿文字圖層的顏色。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 顏色  </span> </span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK顏色值，有無Alpha。 </p> </td> 
 </tr> 
</table>

對於影像和文本圖層，`color=`在應用`rotate=`和`extend=`之前以指定顏色*填充圖層的邊界矩形內的透明和半不透明區域。

## 屬性 {#section-d6e74c36a49547849212e4db8927e678}

層屬性。 應用於當前層，或應用於`layer=comp`時的層0。

*`color`* 假定存在於與像素類型對應的工作顏色空間中 *`color`*。*`color`* 如果圖層影像在合併時具有不同的像素類型，則可精確地轉換。

## 預設 {#section-60611c72876b4c45b5c85ce35608e5ec}

純色和效果圖層沒有預設值；必須指定顏色。 影像和文字圖層的預設值為0,0,0,0（完全透明）。

## 範例 {#section-2d090493f4ec4e188bbc5565aa151a05}

在下列範本片段中，我們將文字背景設定為50%不透明的顏色，並使用相同的顏色在第2層影像周圍新增半透明的10像素邊框：

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 另請參閱 {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), bgColor= [opac=opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)extend= [opac, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)bgc= [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [管理，色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
