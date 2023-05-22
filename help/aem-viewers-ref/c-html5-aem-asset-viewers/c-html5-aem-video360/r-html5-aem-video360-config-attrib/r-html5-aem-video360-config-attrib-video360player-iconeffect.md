---
title: Video360Player.iconeffect
description: Video360查看器的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 818ea14b-4dab-4447-9645-46f2ba82547b
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 7%

---

# Video360Player.iconeffect{#video-player-iconeffect}

Video360查看器的配置屬性。

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *`計數`*][, *`淡`*][, *`自動隱藏`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 當視頻處於暫停狀態時，允許在視頻頂部顯示IconEffect。 在某些設備上，使用本機控制項。 在此情況下， <span class="codeph">像似效應</span> 忽略修改量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 計數</span></span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect顯示和重新顯示的最大次數。 值 <span class="codeph"> -1</span> 指示該表徵圖將無限期地重新顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 淡</span></span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏動畫的持續時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 自動隱藏</span></span> </p> </td> 
   <td colname="col2"> <p> 設定IconEffect在自動隱藏之前保持完全可見的秒數。 即，淡出動畫完成之後和淡出動畫開始之前的時間。 設定為 <span class="codeph"> 0</span> 禁用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

選擇性.

## 預設 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 範例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
