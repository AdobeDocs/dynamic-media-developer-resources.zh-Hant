---
title: SpinView.iconeffect
description: SpinView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e84336da-7f33-4fa9-b881-93b9db4bae8b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *`計數`*][, *`淡`*][, *`自動隱藏`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 啟用 <span class="codeph"> 像似效應</span> 當影像處於重置狀態時顯示在影像的頂部，並且顯示與影像交互的可用操作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定 <span class="codeph"> 像似效應</span> 顯示並重新顯示。 值 <span class="codeph"> -1</span> 指示該表徵圖始終無限期地重新顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 淡</span></span> </p> </td> 
   <td colname="col2"> <p>指定顯示或隱藏動畫的持續時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 自動隱藏</span></span> </p> </td> 
   <td colname="col2"> <p>設定 <span class="codeph"> 像似效應</span> 在自動隱藏前保持完全可見。 即，淡出動畫完成後但淡出動畫開始前的時間。 設定 <span class="codeph"> 0</span> 禁用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選填。

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

`1,1,0.3,3`

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`iconeffect=0`
