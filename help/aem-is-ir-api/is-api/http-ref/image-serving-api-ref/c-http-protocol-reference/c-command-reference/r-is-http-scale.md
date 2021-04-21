---
description: 縮放影像。 相對於全解析度影像，按比例縮放圖層源影像。
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 5%

---


# scale{#scale}

縮放影像。 相對於全解析度影像，按比例縮放圖層源影像。

`scale= *`因子`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 因子</span> </p> </td> 
  <td class="stentry"> <p>比例因子（實數，大於0.0）。 </p></td> 
 </tr> 
</table>

`scale=1`時不應用縮放。 *`factor`* 小於1.0的下縮放和大於1.0的放大會放大源影像。

## 屬性 {#section-3c7eb45527394fe79b1ddba6c1fcca09}

來源影像／遮色片屬性。 如果同時為當前層指定`size=`，則忽略。 覆寫`res=`。 如果為`layer=comp`指定，則套用至層0。 如果圖層未與影像或遮色片相關聯，則忽略此點。

## 預設 {#section-26e64904362342a5a62c5f6598f330c4}

如果未指定，則使用`res=`。 如果未指定`res=`，則不使用縮放來使用影像。

## 另請參閱 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
