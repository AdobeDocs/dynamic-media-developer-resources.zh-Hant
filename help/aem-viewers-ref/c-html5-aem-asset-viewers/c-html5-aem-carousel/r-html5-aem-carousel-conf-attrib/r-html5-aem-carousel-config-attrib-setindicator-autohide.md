---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`限制`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> 限</span>]</span> </p> </td> 
   <td colname="col2"> <p> 根據頁數和運行時元件大小配置自動隱藏行為。 </p> <p> <span class="codeph"> 0</span> 關閉自動隱藏。 </p> <p> <span class="codeph"> 1</span> 啟用自動隱藏。 如果以下至少一個條件變為true，則元件將隱藏其點： </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">帶點的行變寬，或 </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">為此元件設定的頁數超過由 <span class="codeph"><span class="varname"> 限</span></span> 的下界。 </li> 
     </ul> </p> <p> 設定 <span class="codeph"><span class="varname"> 限</span></span> 至 <span class="codeph"> -1</span> 禁用第二個自動隱藏條件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1,10`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
