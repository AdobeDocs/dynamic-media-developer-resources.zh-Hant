---
title: 物件
description: 依名稱選取物件。 依名稱選取指定的暈映群組，並啟動新的MSS。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
TQID: 'https://experienceleague.adobe.com/te9iyNajxDfgvHqqThbVUc7tBItxfMtxhOMl2eCLOsk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 2%

---

# 物件{#obj}

依名稱選取物件。 依名稱選取指定的暈映群組，並啟動新的MSS。

` obj= *`名稱`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">名稱</span> </span> </p> </td> 
  <td class="stentry"> <p>群組名稱或路徑/名稱。 </p> </td> 
 </tr> 
</table>

子群組或個別物件可使用完全合格的群組路徑來選取(也就是指定目標群組或物件的名稱，其前面加上/ （正斜線）分隔)。

如果找不到具有指定名稱的群組/物件，則會採取`attribute::OnObjFail`中指定的動作。

## 屬性 {#section-9463b36e8ff74c81a70c7c2b58927430}

選取範圍指令；MSS分隔符號。 物件選取項會持續存在，直到選取其他物件為止（使用`obj=`或`sel=`）。

群組/物件路徑和名稱不區分大小寫。

## 預設 {#section-0c322850512c4896bb551856a549440e}

開啟新暈映時，會自動選取暈映中包含可轉譯物件的第一個群組。

## 另請參閱 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b)，[attribute：：OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
