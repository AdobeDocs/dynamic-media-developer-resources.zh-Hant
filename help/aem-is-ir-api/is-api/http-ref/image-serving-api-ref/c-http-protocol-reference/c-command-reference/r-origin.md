---
description: 圖層原點。
seo-description: 圖層原點。
seo-title: 來源
solution: Experience Manager
title: 來源
topic: Scene7 Image Serving - Image Rendering API
uuid: a36fc0b6-7744-4c1c-b9f8-4aa31a886bff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 來源{#origin}

圖層原點。

`origin= *`坐標`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標</span> </p></td> 
  <td class="stentry"> <p>從圖層直角的左上角偏移像素(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>與圖層中心的歸一化偏移方向（實數、實數）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>層rect始終包含通過進行的任何修改 `extend=`。

定義圖層矩形的對齊點，該對齊點用於相對於圖層0定點陣圖層矩形 `pos=`。 `originN=0,0` 將圖層原點放在圖層矩形的中心。 `originN=-0.5,-0.5` 而 `origin=0,0` 且是圖層矩形 `originN=0.5,0.5` 的左上角和右下角。

## 屬性 {#section-60f639e36ada43d1abc6bfc100afc925}

層屬性。 應用於當前層，或應用於層0（如果） `layer=comp`。 不受施加到層源 `crop=`的層 `scale=`變換( `rotate=`、、、 `flip=`)的影響。 Overrides `anchor=`. 被效果圖層忽略。

## 預設 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

如果 `origin=` 未指定，則通過將圖層變換應用到影像錨點來確定圖層原點。 如果影像錨點未知，則會使用圖層矩形( `originN=0,0`)的中心。

## 範例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

請參閱範本中的 [範例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另請參閱 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
