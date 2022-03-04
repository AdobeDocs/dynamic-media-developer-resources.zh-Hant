---
description: 選擇選擇錯誤處理。 指定在sel=命令失敗時要執行的操作，因為指定的像素位置不在可選對象的掩碼區域內。
solution: Experience Manager
title: OnFailSel
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 13%

---

# OnFailSel{#onfailsel}

選擇選擇錯誤處理。 指定在sel=命令失敗時要執行的操作，因為指定的像素位置不在可選對象的掩碼區域內。

## 屬性 {#section-cec491e6c5c744f9bfafaaa9d8774f83}

枚舉。

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>繼承自 <span class="codeph"> 預設：:OnFailSel </span>。 </p> </td> 
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
  <td class="stentry"> <p>選擇預設組（包含可轉換對象的視圖層次結構中的第一個組）。 </p> </td> 
 </tr> 
</table>

## 預設 {#section-c25f458f9f8f4236963a95779529e664}

繼承自 `default::OnFailSel` 的子菜單。

## 另請參閱 {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) 。 [屬性：:OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
