---
title: 縮放
description: 縮放影像。 相對於完整解析度影像，以係數縮放圖層來源影像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
TQID: 'https://experienceleague.adobe.com/qC-yBofpV9CNTTjb8Ll1EYV6Q1YA0BUsLLEHadfLAu8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 2%

---

# 縮放{#scale}

縮放影像。 相對於完整解析度影像，以係數縮放圖層來源影像。

`scale= *`因數`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">因素</span> </p> </td> 
  <td class="stentry"> <p>縮放因數（實數，大於0.0）。 </p></td> 
 </tr> 
</table>

`scale=1`時未套用任何縮放。 *`factor`*&#x200B;小於1.0且大於1.0會放大來源影像。

## 屬性 {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Source影像/遮色片屬性。 如果已為目前圖層同時指定`size=`，則略過。 覆寫`res=`。 若指定給`layer=comp`，則套用至圖層0。 如果圖層未與影像或遮色片相關聯，則忽略此項。

## 預設 {#section-26e64904362342a5a62c5f6598f330c4}

如果未指定，則使用`res=`。 如果未指定`res=`，則不會縮放使用影像。

## 另請參閱 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) ， [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
