---
title: 對齊
description: 按名稱選擇對象。 按名稱選擇指定的視頻組並啟動新MSS。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 3%

---

# 對齊{#obj}

按名稱選擇對象。 按名稱選擇指定的視頻組並啟動新MSS。

` obj= *`名稱`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名稱 </span> </span> </p> </td> 
  <td class="stentry"> <p>組名稱或路徑/名稱。 </p> </td> 
 </tr> 
</table>

可以使用完全限定的組路徑(即，通過指定目標組或對象的名稱，前面帶有所有父組，以/（正斜槓）分隔)來選擇子組或單個對象。

如果找不到具有指定名稱的組/對象，則在 `attribute::OnObjFail` 的下界。

## 屬性 {#section-9463b36e8ff74c81a70c7c2b58927430}

選擇命令；MSS分隔符。 對象選擇是永久的，直到選擇了另一個對象， `obj=` 或 `sel=`。

組/對象路徑和名稱不區分大小寫。

## 預設 {#section-0c322850512c4896bb551856a549440e}

當開啟新視頻時，自動選擇包含可呈現對象的視頻中的第一組。

## 另請參閱 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b)。 [屬性：:OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
