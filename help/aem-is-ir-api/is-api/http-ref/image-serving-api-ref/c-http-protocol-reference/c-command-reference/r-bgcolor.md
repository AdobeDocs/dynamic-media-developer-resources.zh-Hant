---
description: 圖層背景顏色。 指定目前圖層的背景顏色和不透明度。
solution: Experience Manager
title: bgColor
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 4%

---


# bgColor{#bgcolor}

圖層背景顏色。 指定目前圖層的背景顏色和不透明度。

`bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 顏色</span></span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK顏色值，有無Alpha。 </p></td> 
 </tr> 
</table>

在套用* `opac=`、`rotate=`和`extend=`後，圖層邊界矩形內的透明和半不透明區域會填入指定的顏色*。

## 屬性 {#section-19dfc13e997f4a33889a1df1e4ad50b9}

層屬性。 應用於當前層，或應用於`layer=comp`時的層0。 被效果圖層忽略。

*`color`* 假定存在於與像素類型對應的工作顏色空間中 *`color`*。*`color`* 如果最終圖層影像具有不同的像素類型，則可精確轉換。

## 預設 {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0（完全透明）。

## 範例 {#section-6e14fcf1d31e432dbdb56b9320904453}

請參閱[color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)。

## 另請參閱 {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), color= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)blendMode=,  [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)，延伸= [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [RotatingColor=Bgc=ColorManagement, Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
