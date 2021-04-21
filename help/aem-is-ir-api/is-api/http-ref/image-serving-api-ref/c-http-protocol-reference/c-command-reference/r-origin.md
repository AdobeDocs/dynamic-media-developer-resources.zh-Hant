---
description: 圖層原點。
solution: Experience Manager
title: 來源
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---


# origin{#origin}

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
>層rect始終包含`extend=`所做的任何修改。

定義圖層矩形的對齊點，該對齊點用於通過`pos=`相對於圖層0定點陣圖層矩形。 `originN=0,0` 將圖層原點放在圖層矩形的中心。`originN=-0.5,-0.5` 而 `origin=0,0` 且是圖層矩 `originN=0.5,0.5` 形的左上角和右下角。

## 屬性 {#section-60f639e36ada43d1abc6bfc100afc925}

層屬性。 應用於當前層，如果`layer=comp`則應用於層0。 不受施加到層源的層變換(`crop=`、`scale=`、`rotate=`、`flip=`)的影響。 覆寫`anchor=`。 被效果圖層忽略。

## 預設 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

如果未指定`origin=`，則通過將圖層變換應用到影像錨點來確定圖層原點。 如果影像錨點未知，則會使用圖層矩形的中心(`originN=0,0`)。

## 範例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

請參閱[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的範例A。

## 另請參閱 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
