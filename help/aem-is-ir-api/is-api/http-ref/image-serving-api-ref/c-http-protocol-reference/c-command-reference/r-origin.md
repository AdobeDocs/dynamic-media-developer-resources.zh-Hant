---
title: 來源
description: 圖層原點。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
TQID: 'https://experienceleague.adobe.com/-wkJjmR-LwxC90IMLNXldXSiaugkaYRyvLS17-nbJAM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 165
ht-degree: 2%

---

# 來源{#origin}

圖層原點。

`origin= *`座標`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">座標</span> </p></td> 
  <td class="stentry"> <p>從圖層矩形(int， int)左上角的畫素位移。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>從圖層矩形中心點的標準化位移（實數、實數）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>圖層矩形一律包含`extend=`的任何修改。

定義圖層矩形的對齊點，用來透過`pos=`相對於圖層0定點陣圖層矩形。 `originN=0,0`將圖層原點放置在圖層矩形的中心。 `originN=-0.5,-0.5`和`origin=0,0`是左上角，`originN=0.5,0.5`是圖層矩形的右下角。

## 屬性 {#section-60f639e36ada43d1abc6bfc100afc925}

圖層屬性。 套用至目前的圖層，或套用至圖層0 （若`layer=comp`）。 不受套用至圖層來源的圖層轉換(`crop=`、`scale=`、`rotate=`、`flip=`)影響。 覆寫`anchor=`。 被效果圖層忽略。

## 預設 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

如果未指定`origin=`，圖層原點會透過將圖層變形套用至影像錨點來決定。 如果影像錨點不明，則會使用圖層矩形( `originN=0,0`)的中心。

## 範例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

檢視[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的範例A。

## 另請參閱 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[錨點=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ， [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143)， [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
