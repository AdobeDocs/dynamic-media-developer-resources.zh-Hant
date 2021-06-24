---
description: SetIndicator.autohide
solution: Experience Manager
title: SetIndicator.autohide
feature: Dynamic Media Classic，檢視器，SDK/API，輪播橫幅
role: Developer,Business Practitioner
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`限制`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> limit</span>]</span> </p> </td> 
   <td colname="col2"> <p> 根據頁面數和執行階段元件大小設定自動隱藏行為。 </p> <p> <span class="codeph"> 0</span> 關閉自動隱藏。 </p> <p> <span class="codeph"> 1</span> 會啟用自動隱藏。如果下列至少一個條件變成true，元件會隱藏其點： </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">包含點的列會變寬至執行時元件寬度，或 </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">為此元件設定的頁數超過<span class="codeph"><span class="varname"> limit</span></span>參數設定的限制。 </li> 
     </ul> </p> <p> 將<span class="codeph"><span class="varname"> limit</span></span>設定為<span class="codeph"> -1</span>會禁用第二個自動隱藏條件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選填。

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1,10`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
