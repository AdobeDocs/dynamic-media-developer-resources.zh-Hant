---
description: 可讓您裁切至內嵌命名路徑的邊界方框。 此裁切會反過來變更影像的大小。
seo-description: 可讓您裁切至內嵌命名路徑的邊界方框。 此裁切會反過來變更影像的大小。
seo-title: cropPathE
solution: Experience Manager
title: cropPathE
topic: Scene7 Image Serving - Image Rendering API
uuid: 4689fd20-dfa0-47eb-8184-cd233f1ac088
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# cropPathE{#croppathe}

可讓您裁切至內嵌命名路徑的邊界方框。 此裁切會反過來變更影像的大小。

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>嵌入層源映像中的路徑名（僅限ASCII）。 </p> <p> <span class="codeph"><span class="varname"> </span></span> pathName是嵌入在層源映像中的路徑的名稱。根據需要自動變換路徑以保持與影像內容的相對對齊。 如果指定了多個<span class="codeph"><span class="varname"> pathName</span></span>，伺服器會裁切到每個路徑的邊界框，一次裁切一個。 在源映像中找不到的<span class="codeph"><span class="varname"> pathName</span></span>都將被忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

層屬性。 如果`layer=comp`，則套用至目前圖層或複合影像。 被效果圖層忽略。

`cropPathE=` 如果在圖層源映像中未找到具有指定名稱的路徑，或者圖層源不是映像，則忽略該路徑。

## 預設 {#section-d1986aa31af14767aeb1b4a57add67f4}

無，因為不再裁切圖層。

## 另請參閱 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[crop](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
