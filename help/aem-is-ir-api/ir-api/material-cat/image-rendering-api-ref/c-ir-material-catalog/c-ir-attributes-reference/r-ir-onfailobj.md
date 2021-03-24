---
description: 物件選取錯誤處理。 指定當obj=命令因指定的路徑無法在暈映物件階層中相符而失敗時要採取的動作。
solution: Experience Manager
title: OnFailObj
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 13%

---


# OnFailObj{#onfailobj}

物件選取錯誤處理。 指定當obj=命令因指定的路徑無法在暈映物件階層中相符而失敗時要採取的動作。

## 屬性 {#section-2c779d9c133a443d9f0aed9fde7b703c}

列舉。

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>繼承自<span class="codeph">預設值：:OnFailObj </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>保留上一個選取範圍. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>取消選擇；將忽略任何嘗試應用材料或顯示／隱藏對象的嘗試。 </p> </td> 
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

## 預設 {#section-a5a95a2b4a204a4eae350e5b544d1513}

如果未定義，則繼承自`default::OnFailObj`。

## 另請參閱 {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ，屬 [性：:OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
