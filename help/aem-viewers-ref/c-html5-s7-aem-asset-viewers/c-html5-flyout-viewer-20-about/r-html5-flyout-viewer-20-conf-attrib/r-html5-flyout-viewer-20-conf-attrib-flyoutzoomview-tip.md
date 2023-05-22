---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 122c6406-6fd7-4e45-bff2-11022a3f2cf7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`持續時間`*[, *`計數`*][, *`淡`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間</span> </span> </p> </td> 
   <td colname="col2"> <p>指定提示文本隱藏之前顯示的秒數。 設定為時 <span class="codeph"> -1</span>，即使用戶激活彈出窗口，消息也始終顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 計數</span> </span> </p> </td> 
   <td colname="col2"> <p>指定查看集合中的新影像時顯示文本的次數。 值 <span class="codeph"> -1</span> 表示在查看集中的任何影像時始終顯示文本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡</span> </span> </p> </td> 
   <td colname="col2"> <p>指定當文本出現或消失時出現的淡入動畫的持續時間。 值 <span class="codeph"> 0</span> 意味著沒有淡出過渡。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

選擇性.

## 預設 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## 範例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
