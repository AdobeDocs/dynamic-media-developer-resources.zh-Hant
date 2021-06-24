---
description: 按名稱選擇對象。 按名稱選擇指定的暈映組並啟動新的MSS。
solution: Experience Manager
title: obj
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# obj{#obj}

按名稱選擇對象。 按名稱選擇指定的暈映組並啟動新的MSS。

` obj= *`名稱`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名稱  </span> </span> </p> </td> 
  <td class="stentry"> <p>組名或路徑/名稱。 </p> </td> 
 </tr> 
</table>

可以使用完全限定的組路徑(即通過指定目標組或對象的名稱，前面加上所有父組，以/（正斜線）分隔)來選擇子組或單個對象。

如果未找到具有指定名稱的組/對象，則執行`attribute::OnObjFail`中指定的操作。

## 屬性 {#section-9463b36e8ff74c81a70c7c2b58927430}

選擇命令；MSS分隔字元。 對象選擇是持續的，直到選擇了另一個對象（具有`obj=`或`sel=`）。

群組/物件路徑和名稱不區分大小寫。

## 預設 {#section-0c322850512c4896bb551856a549440e}

開啟新暈映時，會自動選取暈映中包含可轉譯物件的第一組。

## 另請參閱 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b)，屬 [性：:OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
