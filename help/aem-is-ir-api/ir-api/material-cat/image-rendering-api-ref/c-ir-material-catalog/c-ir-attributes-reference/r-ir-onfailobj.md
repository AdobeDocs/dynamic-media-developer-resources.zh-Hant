---
description: 對象選擇錯誤處理。 指定在obj=命令由於指定的路徑在視頻對象層次結構中無法匹配而失敗時要執行的操作。
solution: Experience Manager
title: OnFailObj
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 14%

---

# OnFailObj{#onfailobj}

對象選擇錯誤處理。 指定在obj=命令由於指定的路徑在視頻對象層次結構中無法匹配而失敗時要執行的操作。

## 屬性 {#section-2c779d9c133a443d9f0aed9fde7b703c}

枚舉。

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>繼承自 <span class="codeph"> 預設：:OnFailObj </span>。 </p> </td> 
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

## 預設 {#section-a5a95a2b4a204a4eae350e5b544d1513}

繼承自 `default::OnFailObj` 的子菜單。

## 另請參閱 {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) 。 [屬性：:OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
