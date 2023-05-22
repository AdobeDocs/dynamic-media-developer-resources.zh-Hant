---
description: 用於裁剪到嵌入的命名路徑的定界框。 此裁剪會反過來更改影像的大小。
solution: Experience Manager
title: 裁剪路徑E
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# 裁剪路徑E{#croppathe}

用於裁剪到嵌入的命名路徑的定界框。 此裁剪會反過來更改影像的大小。

`cropPathE= *`路徑名`*&#42;[, *`路徑名`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 路徑名</span></span> </p> </td> 
   <td colname="col2"> <p>層源影像中嵌入的路徑的名稱（僅限ASCII）。 </p> <p> <span class="codeph"><span class="varname"> 路徑名</span></span> 是層源影像中嵌入的路徑的名稱。 根據需要自動變換該路徑以保持與影像內容的相對對準。 如果多個 <span class="codeph"><span class="varname"> 路徑名</span></span> 指定時，伺服器會裁剪到每個路徑的定界框，一次一個。 任意 <span class="codeph"><span class="varname"> 路徑名</span></span> 將忽略源映像中未找到的內容。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

層屬性。 應用於當前圖層或複合影像 `layer=comp`。 被效果層忽略。

`cropPathE=` 如果在圖層源映像中找不到具有指定名稱的路徑，或者圖層源不是映像，則忽略該路徑。

## 預設 {#section-d1986aa31af14767aeb1b4a57add67f4}

無，因為沒有對圖層進行額外裁剪。

## 另請參閱 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[作物](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab)。 [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
