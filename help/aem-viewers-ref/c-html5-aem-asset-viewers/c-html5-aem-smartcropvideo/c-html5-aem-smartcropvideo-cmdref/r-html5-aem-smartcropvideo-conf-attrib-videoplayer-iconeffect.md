---
title: SmartCropVideoPlayer.iconeffect
description: Smart Crop Video Viewer的配置屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 369e389c-f0e2-405e-b4aa-2f6b9ac8b8ea
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

Smart Crop Video Viewer的配置屬性。

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`計數`*][, *`淡`*][, *`自動隱藏`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 使IconEffect在視頻暫停時顯示在視頻頂部。 在某些設備上，使用本機控制項。 在這種情況下， <span class="codeph"> 像似效應</span> 忽略修改量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 計數</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect顯示和重新顯示的最大次數。 值 <span class="codeph"> -1</span> 指示該表徵圖將無限期地重新顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏動畫的持續時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 自動隱藏</span> </span> </p> </td> 
   <td colname="col2"> <p> 設定IconEffect在自動隱藏之前保持可見的秒數。 即淡入動畫完成後和淡出動畫開始前的時間。 設定 <span class="codeph"> 0</span> 禁用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
