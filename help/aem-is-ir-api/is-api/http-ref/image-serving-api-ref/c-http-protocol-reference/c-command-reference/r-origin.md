---
description: 層原點。
solution: Experience Manager
title: 來源
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# 來源{#origin}

層原點。

`origin= *`坐標`*`

`originN= *`坐標N`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標</span> </p></td> 
  <td class="stentry"> <p>從層矩形的左上角偏移像素(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐標N</span> </p></td> 
  <td class="stentry"> <p>從層直接中心（實數、實數）歸一化偏移。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>層矩形始終包含通過 `extend=`。

定義圖層矩形的對齊點，該對齊點用於通過 `pos=`。 `originN=0,0` 將圖層原點定位在圖層矩形的中心。 `originN=-0.5,-0.5` 和 `origin=0,0` 左上角 `originN=0.5,0.5` 是圖層矩形的右下角。

## 屬性 {#section-60f639e36ada43d1abc6bfc100afc925}

層屬性。 應用於當前圖層，如果 `layer=comp`。 不受層轉換影響( `crop=`。 `scale=`。 `rotate=`。 `flip=`)。 覆蓋 `anchor=`。 被效果層忽略。

## 預設 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

如果 `origin=` 未指定，通過將圖層變換應用於影像錨點來確定圖層原點。 如果影像錨點未知，則圖層矩形的中心( `originN=0,0`)。

## 範例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

請參閱中的示例A [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另請參閱 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[錨=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) 。 [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143)。 [擴展=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
