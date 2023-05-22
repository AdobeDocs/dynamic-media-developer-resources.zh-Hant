---
description: 反向圖層剪輯路徑。 指定當前圖層的排除剪輯路徑。 圖層中位於由clipXPath=定義的區域內的任何部分都呈透明狀態。
solution: Experience Manager
title: 剪輯XPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# 剪輯XPath{#clipxpath}

反向圖層剪輯路徑。 指定當前圖層的排除剪輯路徑。 圖層中位於由clipXPath=定義的區域內的任何部分都呈透明狀態。

`clipXPath= *`pathDefinition`*`

`clipXPathE= *`路徑名`*&#42;[, *`路徑名`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 路徑名</span> </span> </p> </td> 
  <td class="stentry"> <p>層源影像中嵌入的路徑的名稱（僅限ASCII）。 </p></td> 
 </tr> 
</table>

請參閱 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 有關其他資訊，包括 `*`路徑名`*` 和 `*`pathDefinition`*`。

## 屬性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

層屬性。 應用於當前圖層或複合影像 `layer=comp`。 如果忽略 `clipPath=` 未指定。 被效果層忽略。

## 預設 {#section-d1986aa31af14767aeb1b4a57add67f4}

無。

## 另請參閱 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
