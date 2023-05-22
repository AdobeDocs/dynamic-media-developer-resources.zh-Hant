---
description: 將影像與視圖對齊。 在wid=和hei=定義的視圖矩形內對齊複合影像（可能是縮放後，如果也指定了scl=）。
solution: Experience Manager
title: 對齊
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# 對齊{#align}

將影像與視圖對齊。 在wid=和hei=定義的視圖矩形內對齊複合影像（可能是縮放後，如果也指定了scl=）。

` align= *`霍里茲`*, *`變態`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 霍里茲 </span> </span> </p> </td> 
  <td class="stentry"> <p>水準對齊（實數，-1.0..1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 變態 </span> </span> </p> </td> 
  <td class="stentry"> <p>垂直對齊（實數，-1.0..1.0） </p> </td> 
 </tr> 
</table>

指定 `align=-1,-1` 要將複合影像的左上角與視圖的左上角對齊，請指定 `align=1,1` 將影像的右下角與視圖的右下角對齊。 對於標準影像和縮略圖請求，未被複合影像資料覆蓋的視圖的任何區域都會填充 `bgc=`。

## 屬性 {#section-3fbec8206fc944eda4746d8be84f3b41}

查看屬性。 ( `align=` 還用於定義水印影像與應用水印的複合影像之間的對齊方式。) 應用，與當前圖層設定無關。 如果只有其中一個 `wid=` 和 `hei=` 指定時間 `fit=constrain` 或 `fit=stretch`。

## 預設 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`，它將影像居中在視圖矩形中。

## 範例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

以下請求適合 `myImage` 200x200像素視圖矩形。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

如果 `myImage` 正方形，它填充整個視圖矩形。 如果 `myImage` 具有縱向長寬比，它被縮放為200像素高，並在視圖中水準居中。 如果 `myImage` 具有橫向長寬比，它被縮放為200像素寬，並與視圖的上邊緣對齊。 在所有情況下，返回的影像大小都恰好為200x200像素；未被縮放的任何空間 `myImage` 填充 `attribute::BkgColor` （指定bgc=以動態控制背景顏色）。

## 另請參閱 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 。 [黑=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)。 [合適=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)。 [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)。 [水印](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
