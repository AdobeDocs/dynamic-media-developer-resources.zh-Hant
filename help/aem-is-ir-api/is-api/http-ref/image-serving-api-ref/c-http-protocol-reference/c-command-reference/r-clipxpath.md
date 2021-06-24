---
description: 反轉圖層剪輯路徑。 指定當前圖層的排除剪輯路徑。 圖層中由clipXPath=定義的區域內的任何部分都呈現為透明。
solution: Experience Manager
title: clipXPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# clipXPath{#clipxpath}

反轉圖層剪輯路徑。 指定當前圖層的排除剪輯路徑。 圖層中由clipXPath=定義的區域內的任何部分都呈現為透明。

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>層源影像中嵌入的路徑名（僅限ASCII）。 </p></td> 
 </tr> 
</table>

有關其他資訊，請參閱[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)，包括`*`pathName`*`和`*`pathDefinition`*`的說明。

## 屬性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

層屬性。 若`layer=comp`，則套用至目前層或複合影像。 若未指定`clipPath=`，則忽略。 被效果層忽略。

## 預設 {#section-d1986aa31af14767aeb1b4a57add67f4}

無。

## 另請參閱 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
