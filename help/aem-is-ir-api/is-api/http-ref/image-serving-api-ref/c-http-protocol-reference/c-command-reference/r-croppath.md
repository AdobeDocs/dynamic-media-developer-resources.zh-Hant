---
description: 可讓您裁切至內嵌命名路徑的邊界方框。 這個裁切會進而變更影像的大小。
solution: Experience Manager
title: cropPathE
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# cropPathE{#croppathe}

可讓您裁切至內嵌命名路徑的邊界方框。 這個裁切會進而變更影像的大小。

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>層源影像中嵌入的路徑名（僅限ASCII）。 </p> <p> <span class="codeph"><span class="varname"> </span></span> pathName是嵌入到層源映像中的路徑的名稱。根據需要自動轉換該路徑以保持與影像內容的相對對齊。 如果指定了多個<span class="codeph"><span class="varname"> pathName</span></span>，則伺服器會裁切到每個路徑的邊界框，一次裁切一個。 會忽略源映像中找不到的任何<span class="codeph"><span class="varname"> pathName</span></span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

層屬性。 若`layer=comp`，則套用至目前層或複合影像。 被效果層忽略。

`cropPathE=` 如果在圖層源影像中未找到具有指定名稱的路徑，或者圖層源不是影像，則忽略該路徑。

## 預設 {#section-d1986aa31af14767aeb1b4a57add67f4}

無，不會額外裁切圖層。

## 另請參閱 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[裁切](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
