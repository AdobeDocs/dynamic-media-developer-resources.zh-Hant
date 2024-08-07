---
title: clipXPath
description: 反轉的圖層剪裁路徑。 指定目前圖層的排除剪裁路徑。 圖層中，位於clipXPath=所定義區域內的任何部分都會呈現為透明。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# clipXPath{#clipxpath}

反轉的圖層剪裁路徑。 指定目前圖層的排除剪裁路徑。 圖層中，位於clipXPath=所定義區域內的任何部分都會呈現為透明。

`clipXPath= *`pathDefinition`*`

`clipXPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>嵌入圖層來源影像中的路徑名稱（僅限ASCII）。 </p></td> 
 </tr> 
</table>

如需其他資訊，請參閱[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)，包括`*`pathName`*`和`*`pathDefinition`*`的說明。

## 屬性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

圖層屬性。 套用至目前的圖層或複合影像（若為`layer=comp`）。 如果未指定`clipPath=`，則忽略。 被效果圖層忽略。

## 預設 {#section-d1986aa31af14767aeb1b4a57add67f4}

無。

## 另請參閱 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[剪裁路徑=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
