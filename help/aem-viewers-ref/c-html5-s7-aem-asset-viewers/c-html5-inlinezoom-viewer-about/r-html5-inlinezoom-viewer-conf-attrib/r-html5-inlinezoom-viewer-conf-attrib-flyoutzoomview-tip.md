---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`持續時間`*[, *`計數`*][, *`淡化`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">持續時間</span> </span> </p> </td> 
   <td colname="col2"> <p>指定提示文字在隱藏前顯示的秒數。 設定為<span class="codeph"> -1</span>時，即使使用者啟用彈出式視窗，訊息仍一律顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">計數</span> </span> </p> </td> 
   <td colname="col2"> <p>指定檢視集合中的新影像時顯示文字的次數。 值為<span class="codeph"> -1</span>表示檢視該集的任何影像時一律會顯示文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">淡化</span> </span> </p> </td> 
   <td colname="col2"> <p>指定文字出現或消失時所發生之漸隱動畫的持續時間。 值為<span class="codeph"> 0</span>表示沒有淡化切換。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

選擇性.

## 預設 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## 範例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
