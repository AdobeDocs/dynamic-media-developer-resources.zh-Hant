---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: faec00b3-b981-4831-bc97-dff442389133
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`計數`*][, *`淡`*][, *`自動隱藏`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 當影像處於重置狀態且顯示與影像交互的可用操作時，可使IconEffect顯示在影像頂部。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 計數</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect顯示和重新顯示的最大次數。 值 <span class="codeph"> -1</span> 指示該表徵圖始終無限期地重新顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡</span> </span> </p> </td> 
   <td colname="col2"> <p>指定顯示或隱藏動畫的持續時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 自動隱藏</span> </span> </p> </td> 
   <td colname="col2"> <p>設定IconEffect在自動隱藏前保持完全可見的秒數。 即，淡出動畫完成後但淡出動畫開始前的時間。 設定 <span class="codeph"> 0</span> 禁用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-50bcd15223174bb79ce08b31ea03d682}

選填。

## 預設 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## 範例 {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
