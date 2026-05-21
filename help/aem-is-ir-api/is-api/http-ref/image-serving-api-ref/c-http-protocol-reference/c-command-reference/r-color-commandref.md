---
title: 色彩
description: 圖層色彩。 指定純色和效果圖層的前景色和不透明度，以及文字圖層的文字方塊填色色彩。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
TQID: 'https://experienceleague.adobe.com/tjiZfVTztBPgsIYS1SGtVeBxo0Wq1q8Ur-kq3Xtm6og'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 3%

---

# 色彩{#color}

圖層色彩。 指定純色和效果圖層的前景色和不透明度，以及文字圖層的文字方塊填色色彩。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">色彩</span> </span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK色彩值（含或不含Alpha）。 </p> </td> 
 </tr> 
</table>

如果有影像和文字圖層，則在套用* `rotate=`和`extend=`之前，`color=`會以指定的顏色*填滿圖層邊界矩形內的透明和半不透明區域。

## 屬性 {#section-d6e74c36a49547849212e4db8927e678}

圖層屬性。 套用至目前的圖層，或套用至圖層0 （若`layer=comp`）。

假設修飾元&#x200B;*`color`*&#x200B;存在於與&#x200B;*`color`*&#x200B;的畫素型別對應的工作色域中。 如果圖層影像在合併時具有不同的畫素型別，則會精確轉換&#x200B;*`color`*。

## 預設 {#section-60611c72876b4c45b5c85ce35608e5ec}

純色和效果圖層沒有預設值；必須指定顏色。 影像和文字圖層的預設值為0,0，0,0 （完全透明）。

## 範例 {#section-2d090493f4ec4e188bbc5565aa151a05}

在下列範本片段中，文字背景設定為50%不透明顏色，並使用相同顏色在第2層影像周圍新增半透明10畫素邊框：

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 另請參閱 {#section-f0e059f857b64b61ab4f23312b8dc619}

[色彩](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)，[bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)，[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)，[延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)，[bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)，[色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
