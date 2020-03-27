---
description: 反轉圖層剪輯路徑。 指定目前圖層的排除剪輯路徑。 圖層中由clipXPath=定義的區域內的任何部分都呈現為透明。
seo-description: 反轉圖層剪輯路徑。 指定目前圖層的排除剪輯路徑。 圖層中由clipXPath=定義的區域內的任何部分都呈現為透明。
seo-title: clipXPath
solution: Experience Manager
title: clipXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a4062f3f-5dba-4514-acde-e1b7d608a2e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# clipXPath{#clipxpath}

反轉圖層剪輯路徑。 指定目前圖層的排除剪輯路徑。 圖層中由clipXPath=定義的區域內的任何部分都呈現為透明。

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 路 <span class="varname"> 徑定義</span></span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>嵌入層源映像中的路徑名（僅限ASCII）。 </p></td> 
 </tr> 
</table>

請參 [閱clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) ，以取得其他資訊，包括 ` *`pathName`*` 和 ` *`pathDefinition的說明`*`。

## 屬性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

層屬性。 應用於當前圖層或複合影像（如果） `layer=comp`。 如果未指 `clipPath=` 定，則忽略。 被效果圖層忽略。

## 預設 {#section-d1986aa31af14767aeb1b4a57add67f4}

無。

## 另請參閱 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
