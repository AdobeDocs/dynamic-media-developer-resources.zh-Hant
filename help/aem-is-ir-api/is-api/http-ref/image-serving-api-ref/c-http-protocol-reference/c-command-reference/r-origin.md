---
description: 圖層原點。
solution: Experience Manager
title: 來源
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---

# 來源{#origin}

圖層原點。

`origin= *`坐標`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標</span> </p></td> 
  <td class="stentry"> <p>從圖層直角的左上角偏移的像素(int、int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>從層直線中心（實、實）歸一化偏移。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>層直接始終包含`extend=`所做的任何修改。

定義層矩形的對齊點，該對齊點用於通過`pos=`將層矩形相對於層0定位。 `originN=0,0` 將圖層原點置於圖層矩形的中心。`originN=-0.5,-0.5` 且 `origin=0,0` 是圖層矩形的 `originN=0.5,0.5` 左上角，右下角。

## 屬性 {#section-60f639e36ada43d1abc6bfc100afc925}

層屬性。 應用於當前層，如果`layer=comp`則應用於層0。 不受應用於層源的層轉換(`crop=`、`scale=`、`rotate=`、`flip=`)的影響。 覆蓋`anchor=`。 被效果層忽略。

## 預設 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

如果未指定`origin=`，則通過將圖層變換應用到影像錨點來確定圖層原點。 如果影像錨點不是已知的，則使用層矩形的中心(`originN=0,0`)。

## 範例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

請參閱[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的範例A。

## 另請參閱 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[錨點=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
