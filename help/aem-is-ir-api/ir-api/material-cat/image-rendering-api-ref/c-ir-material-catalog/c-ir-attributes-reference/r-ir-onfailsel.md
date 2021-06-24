---
description: 選擇選擇錯誤處理。 指定如果sel=命令失敗，則要採取的操作，因為指定的像素位置不在可選對象的掩碼區域內。
solution: Experience Manager
title: OnFailSel
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 12%

---

# OnFailSel{#onfailsel}

選擇選擇錯誤處理。 指定如果sel=命令失敗，則要採取的操作，因為指定的像素位置不在可選對象的掩碼區域內。

## 屬性 {#section-cec491e6c5c744f9bfafaaa9d8774f83}

列舉。

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>繼承自<span class="codeph">預設值：:OnFailSel </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>保留上一個選取範圍. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>取消選擇；將忽略應用材料或顯示/隱藏對象的任何嘗試。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>傳回錯誤. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>選取預設群組（暈映階層中包含可轉譯物件的第一個群組）。 </p> </td> 
 </tr> 
</table>

## 預設 {#section-c25f458f9f8f4236963a95779529e664}

若未定義，則繼承自`default::OnFailSel`。

## 另請參閱 {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) ，屬 [性：:OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
