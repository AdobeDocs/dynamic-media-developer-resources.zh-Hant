---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic，檢視器，SDK/API，內嵌縮放
role: Developer,Business Practitioner
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
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

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選填。

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
