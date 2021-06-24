---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic，檢視器，SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: 122c6406-6fd7-4e45-bff2-11022a3f2cf7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間</span> </span> </p> </td> 
   <td colname="col2"> <p>指定提示文本在隱藏之前顯示的秒數。 當設定為<span class="codeph"> -1</span>時，即使用戶激活彈出，仍始終顯示消息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 計數</span> </span> </p> </td> 
   <td colname="col2"> <p>指定檢視集合中的新影像時顯示文字的次數。 值<span class="codeph"> -1</span>表示在檢視集合中的任何影像時，一律會顯示文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡出</span> </span> </p> </td> 
   <td colname="col2"> <p>指定文本出現或消失時出現的淡化動畫的持續時間。 值<span class="codeph"> 0</span>表示沒有淡出轉變。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選填。

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
