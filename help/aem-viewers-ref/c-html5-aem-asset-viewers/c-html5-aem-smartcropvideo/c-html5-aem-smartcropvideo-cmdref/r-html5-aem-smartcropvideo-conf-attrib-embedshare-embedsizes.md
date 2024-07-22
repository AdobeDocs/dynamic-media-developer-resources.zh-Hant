---
title: EmbedShare.embedsizes
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: c638d9fd-39bb-4baa-9b3a-99d9bc0307b5
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

智慧型裁切視訊檢視器的設定屬性。

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`寬度`*, *`高度`*[,0|1][; *`寬度`*, *`高度`*[,0|1]]`

指定內嵌共用模式對話方塊中大小下拉式方塊的內嵌大小清單。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">寬度</span> </span> </p> </td> 
   <td colname="col2"> <p> 內嵌寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">高度</span> </span> </p> </td> 
   <td colname="col2"> <p>內嵌高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 指定此清單專案是否應該在下拉式方塊中預先選取。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

選擇性.

## 預設 {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## 範例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
